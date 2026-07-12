# 伤害结算

一次武器命中会拆分为物理、火焰、冰霜、闪电和神圣伤害，再分别经过伤害加成、护甲与抗性结算。

核心结论：
- **元素点伤**（火/冰/雷/圣）会被完整吃到“全局乘区”。
- **原版附魔加伤**（以及模组的“附魔型元素加伤”）在流程末端以“平伤”叠加，基本不吃乘区。
- 火 / 冰 / 雷 / 圣，以及物理破甲的命中阈值，统一按“护甲 / 抗性结算前的原始伤害分量”计算。

---

## 1. 关键术语

一次攻击会同时存在两套“暴击”概念：

- **原版暴击**：下落攻击触发的原版暴击，会提供 $1.5\times$ 的乘数，并且会让“跳劈增伤（leap_attack_damage）”生效。
- **Runeforged 暴击**：由词条 暴击率（以及部分符文词条）触发的随机暴击。触发时不会再额外乘 $1.5\times$，而是给“全局加成百分比”额外加上 $+50\%$（以及额外暴击伤害百分比，如果存在）。

---

## 2. 结算流程

下面用“概念公式”描述流程（省略了一些保护性的 `max(0, …)` 细节）。

### Step 1：物理点伤 + 物理百分比

先把原版暴击从基础物理里剥离出来（避免重复计算），然后叠加模组的物理点伤与物理百分比：

- 去暴击后的原版基础物理：

$$
Base_{noCrit} = \begin{cases}
Base/1.5 & (原版跳劈暴击=true)\\
Base & (原版跳劈暴击=false)
\end{cases}
$$

- 物理合计：

$$
Physical_{total} = (Base_{noCrit} + physical\_damage)\cdot(1 + physical\_damage\_percent/100)
$$

### Step 2：物转元素（Conversion）

- 静态转化（`physical_as_*_percent`）与随机转化（部分符文）相加，但总转化上限为 100%。
- **注意：转化只作用于 Step 1 得到的物理部分，不包含原版附魔加伤。**

转化后：

$$
Physical_{remain} = Physical_{total}\cdot(1 - Conversion_{total}/100)
$$

并分别得到各元素的“转化物理量” $Converted_{fire/ice/lightning/holy}$。

### Step 3：元素点伤 + 元素百分比

对每种元素：

$$
Element = (flatElement + Converted)\cdot(1 + elemental\_damage\_percent/100 + \text{(元素专属百分比)})
$$

（目前只有“神圣元素额外百分比”这一类元素专属项。）

### Step 4：全局乘区（作用于物理与所有元素）

这一步是“最关键的乘区汇总”，会同时作用于 $Physical_{remain}$ 与四种元素伤害。

- **全局加成百分比（同类相加）**：
  - 种族特攻（undead/human/giant 等）
  - 全伤（unique / 符文 military 等）
  - Runeforged 暴击触发时：额外 +50%（以及额外暴击伤害百分比，如果存在）
  - 单持增伤（副手为空）

$$
Global = 1 + AdditiveGlobalPercent/100
$$

- **跳劈乘数**（仅在原版暴击 原版跳劈暴击 时生效）：

$$
Leap = \begin{cases}
1 + leap\_attack\_damage/100 & (原版跳劈暴击=true)\\
1 & \text{否则}
\end{cases}
$$

- **冲刺乘数**（疾跑攻击）：

$$
Dash = \begin{cases}
1 + dash\_attack\_damage/100 & (dashAttack=true)\\
1 & \text{否则}
\end{cases}
$$

- **祝福乘数**（基于世界条件：白天/夜晚/雷雨/异界）：

$$
Blessing = 1 + blessing\_percent/100
$$

- **原版暴击乘数**：

$$
VanillaCrit = \begin{cases}
1.5 & (原版跳劈暴击=true)\\
1 & \text{否则}
\end{cases}
$$

最终非附魔乘区：

$$
Multiplier_{nonEnchant} = VanillaCrit\cdot Global\cdot Leap\cdot Dash\cdot Blessing
$$

并对 $Physical_{remain}$ 与各元素同时乘上该乘区。

### Step 5：诅咒惩罚（最后乘）

$$
Physical_{remain} \*= (1 + cursed\_physical\_damage\_percent/100)
$$

$$
Element \*= (1 + cursed\_elemental\_damage\_percent/100)
$$

### Step 6：附魔加伤（最后平加）

- 模组的“附魔型元素加伤”在此处直接加到对应元素伤害上。
- **原版附魔加伤（originalDamage - basePhysicalDamage）** 保持为“纯物理平伤”，直接加回最终物理伤害。

### Step 7：护甲与抗性

- 物理伤害先结算护甲与护甲韧性；忽视护甲会降低本次计算使用的护甲。
- 元素伤害先使用目标 75% 的护甲和 75% 的护甲韧性结算一次护甲减免，再结算对应元素抗性。
- 元素抗性由目标基础抗性、怪物等级、精英词条和当前状态共同决定，先限制在 -100% 至 95%，最后减去攻击者的元素穿抗。
- 正抗性降低对应元素伤害，负抗性会增加对应元素伤害。详细表格见[元素、抗性与状态](elements-and-resistances.md)。

### Step 8：命中后状态与破甲

- 火、冰、雷、圣的附加效果阈值，统一读取“该元素这一下的原始伤害分量”，不看目标已经结算完护甲 / 抗性后的最终掉血。
- 物理伤害在命中后还会附加 `4` 秒破甲：
  - 阈值为 `5 / 10 / 40`
  - 对应单次新增破甲为 `5% / 10% / 25%`
  - 物理破甲可叠加到 `50%`
  - 它与切割战技的破甲并行结算，都会按“目标原护甲”折算成护甲衰减
  - 怪物来源的物理破甲不对玩家生效；元素特效仍然会正常对玩家生效

---

## 3. 读表时容易踩的坑

- 暴击率 触发的是 **Runeforged 暴击**，它影响的是“全局加成百分比”，不是独立的 $1.5\times$。
- 跳劈伤害 只在 **原版暴击** 时触发；也就是说，它与 暴击率 没有必然关系。
- “元素点伤”会被 Step 4 的全局乘区放大；而“原版附魔加伤”不会被放大，所以后期相对收益会越来越低。

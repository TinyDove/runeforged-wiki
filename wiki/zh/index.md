# Runeforged 中文 Wiki

**适用模组版本：0.2.0　Minecraft：26.1 与 26.2 全版本**

Runeforged（符文锻造）是一个围绕装备成长构建的原版+ ARPG 模组。装备会获得品质、词条和特殊状态；玩家可以用符文石逐步塑造装备，也会面对随世界进度增强的怪物、精英能力、元素抗性与特殊掉落。

本 Wiki 记录模组物品、操作、机制和默认数据。各页面按模组系统组织；具体词条效果、适用对象、使用条件和概率写在对应系统或数据表中。

第一次阅读可以从[快速上手](getting-started/quick-start/index.md)开始；它只介绍系统框架，并链接到各项完整规则。

## 内容索引

| 系统 | 内容 | 页面 |
| --- | --- | --- |
| 装备 | 品质、词条 Tier、材质升阶、灌注与诅咒 | [品质与词条](equipment/quality-and-affixes.md)、[材质升阶](equipment/material-upgrade.md)、[灌注系统](equipment/infusion.md)、[诅咒系统](equipment/curses.md) |
| 通货 | 塑形石等通货的用法、条件与结果 | [符文石与装备塑造](equipment/currency-workflow.md) |
| 武器 | 质变、特殊变体、符文诅咒与战技 | [武器质变](equipment/weapon-transmutation.md)、[特殊武器变体](equipment/special-weapon-variants.md)、[符文诅咒武器](equipment/rune-cursed-weapons.md) |
| 战斗 | 伤害顺序、护甲、抗性、元素与状态 | [伤害结算](combat/damage-pipeline.md)、[元素、抗性与状态](combat/elements-and-resistances.md) |
| 怪物 | 等级、属性成长、精英能力与奖励 | [怪物等级](monsters/monster-levels.md)、[精英怪](monsters/elites.md) |
| 获取 | 怪物、宝箱、钓鱼与交易数据 | [怪物掉落](obtaining/monster-drops.md)、[宝箱与交易](obtaining/chests-and-trades.md)、[钓鱼](obtaining/fishing.md) |
| 数据表 | 全词条、武器变体、通货和默认配置 | [数据库](reference/index.md) |
| 指令 | 玩家可用的查询、等级与信息指令 | [玩家指令](reference/commands.md) |

!!! note "服务器配置"
    Wiki 展示模组的**默认配置**。服务器或整合包可以修改 `config/runeforged-*.json`；遇到不一致时，以服务器实际配置和游戏内结果为准。

# 安装与兼容性

## 当前目标环境

| 项目 | 要求 |
| --- | --- |
| Minecraft | 26.1 与 26.2 全版本 |
| 模组加载器 | 对应 Minecraft 版本可用的 Fabric Loader |
| Fabric API | 对应 Minecraft 版本可用的 Fabric API |
| Java | 25 或更高 |
| Runeforged | 0.2.0 |

JEI 和 Mod Menu 是可选兼容模组。JEI 可用于查看配方；符文石能否作用于某件装备，取决于装备品质、词条数量和特殊状态。

## 客户端与服务器

Runeforged 的环境声明为客户端和服务端均需要。多人游戏中应确保服务端与所有玩家使用相同模组版本；默认配置由服务端规则决定。

## 配置文件

首次运行后会在实例的 `config/` 下生成：

- `runeforged-general.json`
- `runeforged-affixes.json`
- `runeforged-monsters.json`
- `runeforged-compat.json`

服务器数值与 Wiki 不一致时，先检查这些文件。默认情况下，版本升级不会强制覆盖玩家已有配置。

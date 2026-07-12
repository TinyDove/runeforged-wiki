# 安装与兼容性

## 当前目标环境

| 项目 | 要求 |
| --- | --- |
| Minecraft | 26.2 RC / 正式版系列 |
| 模组加载器 | Fabric Loader 0.19.3 或更高 |
| Fabric API | 0.152.1+26.2 或兼容版本 |
| Java | 25 或更高 |
| Runeforged | 0.2.0 |

JEI 和 Mod Menu 是可选兼容模组。JEI 用于查看可展示的配方；部分符文石和装备塑造属于动态配方，最终可用条件仍以合成预览和本 Wiki 规则为准。

## 客户端与服务器

Runeforged 的环境声明为客户端和服务端均需要。多人游戏中应确保服务端与所有玩家使用相同模组版本；默认配置由服务端规则决定。

## 配置文件

首次运行后会在实例的 `config/` 下生成：

- `runeforged-general.json`
- `runeforged-affixes.json`
- `runeforged-monsters.json`
- `runeforged-compat.json`

服务器数值与 Wiki 不一致时，先检查这些文件。默认情况下，版本升级不会强制覆盖玩家已有配置。


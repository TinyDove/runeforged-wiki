# 安装与兼容性

## 支持环境

下表中的 Fabric Loader 是最低可用版本，不要求使用当前最新版。Fabric API 只需选择与 Minecraft 版本完全对应的可用版本。

| Minecraft | Fabric Loader 最低版本 | Fabric API | Java |
| --- | --- | --- | --- |
| 1.21.11 | 0.17.3 | 对应 1.21.11 的版本 | 21 或更高 |
| 26.1 | 0.18.4 | 对应 26.1 的版本 | 25 或更高 |
| 26.2 | 0.18.4 | 对应 26.2 的版本 | 25 或更高 |
| 26.3 | 0.18.4 | 对应 26.3 的版本 | 25 或更高 |

上述 Minecraft 版本目前均使用 Runeforged 0.2.2，但安装时仍须选择文件名中 Minecraft 版本完全对应的 JAR。开发与测试可能使用更新的 Fabric Loader 或 Fabric API，这不代表玩家必须升级到相同版本。

!!! warning "世界版本"
    不支持把已经由 Minecraft 26.x 打开或保存的世界直接降级到 1.21.11。切换 Minecraft 版本前请备份世界，并使用独立实例。

JEI 和 Mod Menu 是可选兼容模组。JEI 可用于查看配方；符文石能否作用于某件装备，取决于装备品质、词条数量和特殊状态。

## 客户端与服务器

Runeforged 的环境声明为客户端和服务端均需要。多人游戏中应确保服务端与所有玩家使用相同 Minecraft 专用构建的 Runeforged；默认配置由服务端规则决定。

## 配置文件

首次运行后会在实例的 `config/` 下生成：

- `runeforged-general.json`
- `runeforged-affixes.json`
- `runeforged-monsters.json`
- `runeforged-compat.json`

服务器数值与 Wiki 不一致时，先检查这些文件。

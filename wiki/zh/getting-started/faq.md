# 常见问题

## 支持哪些 Minecraft 版本？

Runeforged 0.2.2 支持 Minecraft 1.21.11、26.1、26.2 与 26.3。下载时应选择文件名与 Minecraft 版本完全对应的 Runeforged JAR 和 Fabric API。

## Fabric Loader 和 Fabric API 必须使用最新版吗？

不需要。Minecraft 1.21.11 的最低 Fabric Loader 是 0.17.3；26.1、26.2 与 26.3 的最低版本是 0.18.4。Fabric API 只需使用与 Minecraft 版本对应的兼容包；开发时采用的较新版本不是强制要求。

## 客户端和服务器都需要安装吗？

需要。多人游戏中，服务端与所有玩家应安装相同 Minecraft 专用构建的 Runeforged，并使用相互兼容的 Minecraft、Fabric Loader 和 Fabric API。

## 可以把 26.x 世界直接降级到 1.21.11 吗？

不支持。不同 Minecraft 版本应使用独立实例；切换版本前请备份世界，不要用 1.21.11 直接打开已经由 26.x 保存的世界。

## 为什么 Wiki 数值与服务器不同？

Wiki 展示默认配置。服务器或整合包可以修改 `runeforged-general.json`、`runeforged-affixes.json`、`runeforged-monsters.json` 和 `runeforged-compat.json`。

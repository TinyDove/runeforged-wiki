# Installation & Compatibility

## Supported Environment

The Fabric Loader versions below are minimum usable versions, not requirements to install the current latest release. For Fabric API, use an available build that exactly matches the selected Minecraft version.

| Minecraft | Minimum Fabric Loader | Fabric API | Java |
| --- | --- | --- | --- |
| 1.21.11 | 0.17.3 | A build for 1.21.11 | 21 or newer |
| 26.1 | 0.18.4 | A build for 26.1 | 25 or newer |
| 26.2 | 0.18.4 | A build for 26.2 | 25 or newer |
| 26.3 | 0.18.4 | A build for 26.3 | 25 or newer |

All listed Minecraft versions currently use Runeforged 0.2.2, but you must still select the JAR whose filename exactly matches your Minecraft version. Development and testing may use newer Fabric Loader or Fabric API versions; players are not required to use those exact versions.

!!! warning "World versions"
    Worlds opened or saved by Minecraft 26.x are not supported for direct downgrade to 1.21.11. Back up worlds and use a separate instance before changing Minecraft versions.

JEI and Mod Menu are optional compatibility mods. JEI can display recipes; whether a Rune Stone can affect an item depends on its quality, affix count, and special state.

## Client and Server

Runeforged is required on both the client and server. In multiplayer, the server and every player should use the same Minecraft-specific Runeforged build. Default configuration is controlled by the server.

## Configuration Files

The first launch creates these files under `config/`:

- `runeforged-general.json`
- `runeforged-affixes.json`
- `runeforged-monsters.json`
- `runeforged-compat.json`

Check these files when server values differ from this wiki.

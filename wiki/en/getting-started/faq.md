# Frequently Asked Questions

## Which Minecraft versions are supported?

Runeforged 0.2.2 supports Minecraft 1.21.11, 26.1, 26.2, and 26.3. Install the Runeforged JAR and Fabric API build made for your exact Minecraft version.

## Must Fabric Loader and Fabric API be the latest versions?

No. The minimum Fabric Loader is 0.17.3 for Minecraft 1.21.11 and 0.18.4 for Minecraft 26.1, 26.2, and 26.3. Fabric API only needs to be a compatible build for the selected Minecraft version; newer development versions are not mandatory for players.

## Is the mod required on both client and server?

Yes. The server and all players should use the same Minecraft-specific Runeforged build and mutually compatible versions of Minecraft, Fabric Loader, and Fabric API.

## Can I directly downgrade a 26.x world to 1.21.11?

No. Use separate instances for different Minecraft versions, back up the world before changing versions, and do not open a world saved by 26.x directly in 1.21.11.

## Why do wiki values differ from a server?

The wiki documents default configuration. A server or modpack can change `runeforged-general.json`, `runeforged-affixes.json`, `runeforged-monsters.json`, and `runeforged-compat.json`.

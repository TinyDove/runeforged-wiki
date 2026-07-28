# Player Commands

Runeforged player commands begin with `/rf`. Ordinary query and guide commands require no administrator permission.

World-level management commands are player-only and cannot be run directly from the server console. `set` requires GameMaster permission or singleplayer-owner status and also requires Creative mode. `extra` and `clear` require GameMaster permission or singleplayer-owner status but do not require Creative mode.

| Command | Result |
| --- | --- |
| `/rf help` | Command index |
| `/rf guide` | In-game stage-hint index |
| `/rf guide start` | First Steps hints |
| `/rf guide forge` | Gear Forging hints |
| `/rf guide weapon` | Weapons and Skills hints |
| `/rf guide elements` | Element Counters hints |
| `/rf guide late` | Late Paths hints |
| `/rf level` | Base monster level at the current position and every contributing factor; excludes per-mob random and Elite bonus levels |
| `/rf level restore` | Clears the personal death level-down adjustment |
| `/rf level set <1–100>` | Locks the world's base level; requires world-level permission and Creative mode |
| `/rf level extra <1–100>` | Adds a world monster level to the calculated or locked base level and raises its cap by the same amount; requires world-level permission |
| `/rf level clear` | Clears both the world base-level lock and world monster extra level; requires world-level permission |
| `/rf dps` | Main-hand weapon's theoretical panel DPS, hit or shot damage, speed or charge time, and rating |
| `/rf info` | Quick-reference index for elemental and Physical Damage |
| `/rf info fire` | Fire weaknesses, resistances, environment, and effect |
| `/rf info frost` | Frost weaknesses, resistances, environment, and effect |
| `/rf info lightning` | Lightning weaknesses, resistances, environment, and effect |
| `/rf info holy` | Holy weaknesses, resistances, and effect |
| `/rf info physical` | Physical armor-break effect |

## DPS Panel Scope

Melee DPS includes expected Critical Strikes, the active Blessing, and active Single-Wield Damage. It excludes Slayer Damage, Elemental Resistance Penetration, Armor Penetration, Leap/Dash conditional damage, Attack Range, and other unstable factors.

Ranged DPS includes expected Critical Strikes, expected extra projectiles, and the active Blessing. It excludes draw/reload speed, Long-Range Damage, Slayer Damage, and other conditional factors. This is a standardized equipment-comparison panel, not final DPS against a specific target.

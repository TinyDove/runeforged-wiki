# Monster Levels

A monster's final level combines area level, world progression, random bonus levels, and Elite modifiers. Level affects monster stats, equipment quality, currency drops, and Infusion Value.

## Area Level

`floor(Local Difficulty × 5 + horizontal distance + vertical depth/height + dimension bonus)`

The default horizontal cycle is 1,000 blocks for `+10` levels, with no contribution below zero. The Nether and End each have a default `+10` dimension bonus.

In the Overworld, Depth contribution begins below `Y=50`. From Y=50 to Y=0, every full `10` blocks downward adds `1` level. Below Y=0, every further `5` blocks adds `1` level. Depth contribution is normally capped at `+15`. The Nether and End ignore Depth contribution.

Height contribution begins above `Y=100`. Every full `20` blocks upward adds `1` level, normally capped at `+15`. After the Ender Dragon is defeated for the first time, Depth contribution is calculated at twice the rate and its cap rises to `+30`; the horizontal Distance cap also doubles. Height keeps its normal rule.

`/rf level` separates Local Difficulty, Distance, Depth, Height, Dimension, Time, boss progression, manual adjustment, and death level-down.

## World Progression

| Rule | Default |
| --- | ---: |
| Days per +1 time level | 10 days |
| Time-level cap | 10 |
| Ender Dragon bonus | +10 |
| Final global cap | 100 |
| Maximum random spawn bonus | 5 |
| Random bonus stage factor | 2.0 |

## World-Level Management

Authorized players can lock or add world levels:

- `/rf level set <1–100>` locks the world base level and replaces area, time, and boss-progression calculation.
- `/rf level extra <1–100>` adds the specified amount to either the calculated or locked base level.
- `/rf level clear` clears both the base-level lock and the extra level.

`set` requires GameMaster permission or singleplayer-owner status, and the player must be in Creative mode. `extra` and `clear` require GameMaster permission or singleplayer-owner status but do not require Creative mode. All three management commands are player-only and cannot be run directly from the server console.

The extra level is persistent world data shared across dimensions. It also raises the current base-level cap by the same amount: if the ordinary cap is 100 and the extra level is `+25`, the effective cap is 125. When a lock and extra level coexist, the final base level is the locked level plus the extra level.

Setting or clearing the extra level does not recalculate monsters whose levels have already been generated and saved. The new value applies when a monster is first assigned a level afterward.

`/rf level` lists the lock and extra level separately. Per-mob random and Elite bonus levels are still added after the base level.

## Stat Scaling

| Stat | Per-level scaling |
| --- | ---: |
| Max Health | +5% |
| Attack Damage | +2% |
| Armor | Hostile monsters +0.1, through level 100 |

At levels 25, 50, 75, and 100, each reached step also grants +25% base Max Health, +1 Attack Damage, +2 Armor, and +2 Armor Toughness. Both health components use the monster's base Max Health.

Ordinary monsters begin with 10% Frost, Lightning, and Holy Resistance and gain another 5% at each 25-level step. Fire Resistance does not scale with level. Species-specific values are listed under [Elements, Resistances & Status Effects](../combat/elements-and-resistances.md).

## Temporary Death Level-Down

If a player dies within the default 10-second window after monster damage, their nearby base level is temporarily lowered. The first adjustment is `-2`; repeated deaths progress toward `-5` or `-10`, with a minimum of `-10`. One level recovers every half game day by default. `/rf level restore` immediately clears the player's active death level-down. This adjustment changes the base level used near that player.

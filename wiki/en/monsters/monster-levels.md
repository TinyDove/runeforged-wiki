# Monster Levels

A monster's final level combines area level, world progression, random bonus levels, and Elite modifiers. Level affects monster stats, equipment quality, currency drops, and Infusion Value.

## Area Level

`floor(Local Difficulty × 5 + horizontal distance + vertical depth/height + dimension bonus)`

The default horizontal cycle is 1,000 blocks for `+10` levels, with no contribution below zero. The Nether and End each have a default `+10` dimension bonus.

In the Overworld, Depth contribution begins below `Y=50`. From Y=50 to Y=0, every full `10` blocks downward adds `1` level. Below Y=0, every further `5` blocks adds `1` level. Depth contribution is normally capped at `+15`. The Nether and End ignore Depth contribution.

Height contribution begins above `Y=100`. Every full `20` blocks upward adds `1` level, normally capped at `+15`.

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

A server command can lock or add levels; a lock takes priority over normal progression.

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

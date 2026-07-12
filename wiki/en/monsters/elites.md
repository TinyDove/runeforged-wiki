# Elite Monsters

This page lists Elite generation, scaling, rewards, and every Elite Affix.

## Generation Chance

`P = min(100%, 1% + Base Monster Level × 0.02% + Ender Dragon bonus)`

- Defeating the Ender Dragon adds `0.5` percentage points.
- Giant variants double the chance.
- One random Elite may exist per chunk by default; guaranteed Elites do not use this cap.
- Wardens and mobs tagged as guaranteed Elites always become Elite. Ender Dragons, Withers, and Wardens have exactly three affixes.
- Summoning Aura reinforcements cannot become Elite.

## Affix Count Algorithm

Random Elites choose 1–4 affixes by weight. Before the Ender Dragon, base weights are `10 / 4 / 2 / 0.5`; afterward they are `10 / 5 / 2.5 / 1`.

Let the roll level be `L`; negative values are treated as `0`, and the default world base-level cap is `100`. Apply these multipliers, then normalize all four weights into probabilities:

| Level | 1 affix | 2 affixes | 3 affixes | 4 affixes |
| --- | --- | --- | --- | --- |
| `L < 25` | base | `×(0.75 + L/100)` | `×(0.50 + L/100)` | `×(L/100)` |
| `25 ≤ L ≤ 50` | `×(1 - (L-25)/100)` | `×(1 + (L-25)/100)` | base | base |
| `L > 50` | `×(1 - (L-25)/100)` | `×(1 + (L-25)/100)` | `×(1 + (L-50)/100)` | `×(1 + (L-50)/100)` |

Before the Ender Dragon:

| Base level | 1 | 2 | 3 | 4 |
| ---: | ---: | ---: | ---: | ---: |
| 0 | 71.43% | 21.43% | 7.14% | 0% |
| 25 | 60.61% | 24.24% | 12.12% | 3.03% |
| 50 | 50.00% | 33.33% | 13.33% | 3.33% |
| 75 | 35.40% | 42.48% | 17.70% | 4.42% |
| 100 | 18.87% | 52.83% | 22.64% | 5.66% |

After the Ender Dragon:

| Base level | 1 | 2 | 3 | 4 |
| ---: | ---: | ---: | ---: | ---: |
| 0 | 66.67% | 25.00% | 8.33% | 0% |
| 25 | 54.05% | 27.03% | 13.51% | 5.41% |
| 50 | 43.48% | 36.23% | 14.49% | 5.80% |
| 75 | 29.63% | 44.44% | 18.52% | 7.41% |
| 100 | 15.15% | 53.03% | 22.73% | 9.09% |

Guaranteed non-boss Elites use `L - 10`; in the Nether or End they use another `-10`. Ender Dragons, Withers, and Wardens skip this count roll.

## Level and Trait Conflicts

- After the count is chosen, eligible affixes are drawn uniformly without replacement. Survival, Offense, and Aura categories have no separate selection weights.
- Giant is excluded because it is a separate variant.
- Neutral mobs eligible for Elite status cannot draw Summoning Aura, Command Aura, or Slowing Aura.
- A candidate is skipped if the size increase from the resulting affix set would not fit in the mob's space.
- A random Elite gains `+10` levels per affix; a guaranteed Elite gains `+5` per affix.
- Giant variants gain another `+5` levels.
- Elemental Resistance and the four single-element Resistance affixes are mutually exclusive.
- Haste conflicts with Berserk; Lightning Pulse conflicts with Fire Pulse.
- Ender Dragons, Withers, and Wardens are guaranteed Elemental Resistance and cannot receive Revival, Command Aura, Summoning Aura, or Damage Transfer.

## Despawn Rules

Within 32 blocks of the nearest player, despawn timers reset. A random Elite that has never fought a player waits 45 seconds while 32–128 blocks away before vanilla distance-despawn checks; one that has fought waits 10 minutes. Beyond 128 blocks, the final waits are 5 seconds and 5 minutes respectively. Forced, guaranteed, or persistent Elites do not use these timers.

## Stat Scaling and Regeneration

- Each Elite Affix adds `+50%` Max Health: `Final Max Health = Base Max Health × (1 + 0.5 × affix count)`.
- Each survival-category affix adds `+15%` size.
- Every Elite Affix adds `+0.5` Armor Toughness.
- Physical Resistance grants `50%` Physical Damage reduction.
- Heavy Armor grants `+10` Armor and `+10` Armor Toughness and doubles Armor Penetration and Armor reduction against it.
- Haste grants `+25%` Movement Speed and `+100%` Knockback Resistance.
- Berserk grants `+20%` Movement Speed and `+20%` Attack Speed.

A non-boss Elite that has taken no damage for 10 seconds heals `1%` of final Max Health each second.

Revival heals `2%` per second of Max Health excluding the health added by Elite Affixes, clamped to 1–4 health per tick. After 5 seconds without taking damage, it additionally heals `4%` of that same base each second with no 1–4 clamp.

## Loot and Experience

Loot level follows the world monster-level cap: 50 by default; 75 after the Wither but before the Ender Dragon; 100 after the Ender Dragon.

- Elites perform four extra base-loot rolls.
- Currency drop attempts equal `Elite Affix count × 5`.
- Elite experience multiplies the level-scaled experience.
- Weapon-using Elites retain their main-hand drop check.
- Armor-using Elites check only their highest-value worn armor piece, at `5% + 5% × affix count`.

### Extra Elite Rewards

| Affixes | Extra reward |
| --- | --- |
| 1 | Roll 1–2 times from Shaping Stone ×1 / Reinforcement Stone ×1 / Reforging Stone ×1; then 1–2 more 50% rolls from the same pool |
| 2 | Guaranteed 1–2 Tempering Stones; then 1–2 50% rolls from Tempering ×1 / Stripping ×1 / Alien Gem ×1 / Reforging ×1 / Reinforcement ×2 / Shaping ×2 |
| 3 | Guaranteed 1–2 Tempering and 1–2 Stripping Stones; 2–3 50% rolls from the two-affix pool; 25% for one Penance Stone / Edict Stone / Sealed Gem / Infusion Gem |
| 4+ | 3–5 rolls from Tempering ×1 / Alien Gem ×1 / Reforging ×1 / Reinforcement ×2 / Shaping ×2 / Stripping ×1; one guaranteed Penance/Edict/Sealed/Infusion item with 25% for another; 10% for one Ascension Stone |

Celestial Fragment is independent: `1%` at two affixes, `5%` at three, and `15%` at four or more.

## Complete Elite Affix List

| Affix | Effect |
| --- | --- |
| Physical Resistance | 50% less Physical Damage taken |
| Heavy Armor | +10 Armor, +10 Armor Toughness; Armor Penetration and reduction are twice as effective |
| Fire Resistance | Fire +80%, other elements +20%; Fire base minimum 75%; Fire penetration doubled |
| Frost Resistance | Frost +80%, other elements +20%; Frost base minimum 75%; Frost penetration doubled |
| Lightning Resistance | Lightning +80%, other elements +20%; Lightning base minimum 75%; Lightning penetration doubled |
| Holy Resistance | Holy +80%, other elements +20%; Holy base minimum 75%; Holy penetration doubled |
| Elemental Resistance | +40% all elemental resistance; base minimum 40% |
| Revival | 2% base Max Health each second, clamped to 1–4; another 4% after 5 seconds without damage |
| Leech | Heals for 50% of total damage dealt |
| Haste | +25% Movement Speed, +100% Knockback Resistance |
| Berserk | +20% Movement Speed and Attack Speed |
| Shatter | +25% all attack damage, stronger knockback, and interrupts shields |
| Lightning Pulse | Every 4 seconds, warns then strikes; +50% Lightning Resistance |
| Fire Pulse | Every 4 seconds, warns then erupts and ignites; +50% Fire Resistance |
| Slowing Aura | Applies Slowness I each second to hostile targets within 8 blocks |
| Healing Denial Aura | Prevents hostile targets within 8 blocks from healing |
| Command Aura | Buffs self and nearby allied monsters' speed, damage, Knockback Resistance, and healing |
| Summoning Aura | In combat, attempts one reinforcement every 8 seconds; maximum four within 16 blocks |
| Damage Transfer | Transfers 80% of incoming damage to other monsters within 4 blocks |

Giant is a separate monster variant, not an Elite Affix: +5 levels, +20 base health, +50% size, +25% Movement Speed, double Elite chance, ×1.5 Runeforged drop chance, ×2 experience, and one extra base-loot roll.

## Detailed Aura and Pulse Rules

- **Damage Transfer:** splits 80% among other monsters within 4 blocks; the Elite takes 20%. With no valid target, it does not activate.
- **Healing Denial Aura:** cancels healing for hostile targets within 8 blocks, including Holy healing and Purification On-Kill Heal.
- **Command Aura:** each second grants self and allied monsters within 8 blocks +10% Movement Speed, +10% Attack Damage, +50% Knockback Resistance, and 0.5% base Max Health healing per second. Attribute buffs last 2 seconds and refresh in range.
- **Summoning Aura:** while in combat, attempts one reinforcement every 8 seconds, with at most four linked reinforcements within 16 blocks. Reinforcements inherit base level and cannot roll Elite.
- **Slowing Aura:** applies Slowness I for 2 seconds, once per second, within 8 blocks.
- **Pulses:** every 4 seconds with a 2-second warning, centered within one block of the target. They hit players and other non-monster-faction targets, never the Elite itself. Lightning Pulse has a 1.5-block radius and deals the greater of 2 or `Attack Damage × 0.75`. Fire Pulse has a 1.75-block radius and deals the greater of 1.5 or `Attack Damage × 0.5`, igniting for 4 seconds.

See [Elements, Resistances & Status Effects](../combat/elements-and-resistances.md) for resistance order.

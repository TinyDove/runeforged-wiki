# Elements, Resistances & Status Effects

Weapons can gain Elemental Damage from regular Affixes, Physical conversion, or [Elemental Enchantments](elemental-enchantments.md).

Resistance is measured in percent: positive values reduce damage and negative values are weaknesses. Base resistance, Elite resistance, and status modifiers are clamped to `-100%–95%`; Elemental Resistance Penetration is subtracted afterward, so effective resistance can fall below `-100%`.

## Base Resistances

### Fire

- Arthropods `-50%`
- Slimes `-50%`
- Snow/Frost mobs `-100%`
- Nether mobs `+50%`
- Witches `-100%`
- Bogged `+50%`
- Silverfish `-50%`
- Other ordinary monsters `0%`, with no level scaling

### Frost

- Nether mobs `-100%`
- Snow/Frost mobs `+50%`
- Creepers `-50%`
- Endermen `-50%`
- Other ordinary monsters `10% + level bonus`

### Lightning

- Aquatic mobs `-50%`
- Metal mobs `-100%`
- Entities wearing conductive armor `-50%`
- Creepers `+50%`
- Witches `+50%`
- Phantoms `-50%`
- Endermen use default resistance

### Holy

- Undead `-100%`
- Illagers `-50%`
- End mobs `+50%`, except the Ender Dragon uses default resistance
- Villagers `+75%`
- Iron Golems `+75%`
- Witches `+75%`
- Endermen `+50%`

## Status and Environment Modifiers

- In water: Fire `+25%`, Frost `-25%`, Lightning `-25%`.
- Exposed to rain: Lightning `-25%`; this is the same environment weakness as water and does not stack with it.
- Burning: Frost `-25%` and Physical resistance `-10%`.
- Frost Slow: Fire `-25%` and Frost `-10%`.
- Lightning-struck state: all elemental resistances `-15%`, plus `+15%` incoming Physical melee/projectile damage.
- Holy defensive buff: all elemental resistances `+15%`.

## Elemental Effects

| Damage type | On-hit effect |
| --- | --- |
| Physical | 4-second Armor Break: raw Physical Damage of 5/10/40 adds 5%/10%/25%, stacking to 50% |
| Fire | Stacking burn for 1–4 seconds at 1–4 damage per second; burning also causes Frost Resistance -25% and Physical Resistance -10% |
| Frost | Slowness II for 0.5–4 seconds; causes Fire Resistance -25% and Frost Resistance -10%; interrupts Creeper explosions and Blaze charging and prevents Enderman teleporting |
| Lightning | 5%–20% chance to strike for extra Lightning Damage equal to 50% of the attack's total damage and apply -15% all elemental and Physical resistance; chance doubles during thunderstorms |
| Holy | 20%–100% chance to heal the attacker for 1 and grant +15% all elemental resistance for 4 seconds |

Effect strength scales with the matching raw damage bucket from 0 to 40, reaching maximum at 40.

## Elite Affix Resistance

### Elemental Resistance

Adds `+40%` to all four elements and sets a `40%` minimum during the base-resistance stage. Status effects and penetration can still reduce the result below 40%.

### Single-Element Resistance

Fire, Frost, Lightning, or Holy Resistance adds `+80%` to its main element and `+20%` to the other three. The main element has a `75%` base-stage minimum, and penetration of that element is doubled.

For example, `20%` Fire penetration acts as `40%` against a Fire Resistance Elite but remains `20%` for its other elements.

### Pulse Resistance

Fire Pulse adds `+50%` Fire Resistance; Lightning Pulse adds `+50%` Lightning Resistance.

## Resistance Order

Elemental damage first passes through `75%` Armor and `75%` Armor Toughness, then resistance:

1. Base resistance: ordinary monsters use `10% + level bonus` for Frost, Lightning, and Holy, while Fire is `0%` without level scaling.
2. Add Elite Affix resistance.
3. Apply the base-stage minimum from Elemental or single-element Resistance.
4. Add status and environment modifiers.
5. Clamp to `-100%–95%`.
6. Subtract Elemental Resistance Penetration.

`Final damage = max(0, post-Armor damage × (1 - effective resistance / 100))`

# Elemental Enchantments

Runeforged adds Fire, Low Temperature, Lightning, and Holy weapon Enchantments. Each adds matching Elemental Damage on hit and uses the same level progression.

## Levels and Damage

| Enchantment Level | Extra Elemental Damage |
| --- | ---: |
| I | `+1.0` |
| II | `+1.5` |
| III | `+2.0` |
| IV | `+2.5` |
| V | `+3.0` |

This damage scales with the strength of a partially charged attack. It is added after the main weapon multipliers, so it does not benefit from Physical/Elemental Damage %, Slayer Damage, Blessings, All Damage, Runeforged Critical Strikes, Single-Wield, Leap, or Dash Attack Damage.

Enchantment damage still passes through Elemental Armor and the matching Resistance, and contributes to the damage strength used by that Element's on-hit effect. See [Damage Calculation](damage-pipeline.md) for its exact position and [Elements, Resistances & Status Effects](elements-and-resistances.md) for Elemental effects.

## The Four Enchantments

| Enchantment | Added Damage | Matching On-Hit Effect |
| --- | --- | --- |
| Fire | Fire Damage | Stacks burning; burning lowers Frost and Physical Resistance |
| Low Temperature | Frost Damage | Slows and lowers Fire and Frost Resistance; can suppress certain monster abilities |
| Lightning | Lightning Damage | Can trigger an extra lightning strike and lower all Elemental and Physical Resistance |
| Holy | Holy Damage | Can restore Health and briefly raise the attacker's all-Element Resistance |

See [Elements, Resistances & Status Effects](elements-and-resistances.md) for exact weaknesses, Resistances, durations, and proc chances.

## Eligibility and Sources

- Maximum level is V.
- They primarily target melee weapons; actual support is limited to weapons that accept sharp-weapon Enchantments.
- They can appear at the Enchanting Table, in random loot, from Villager trades, and on Enchanted Books. They are not Treasure Enchantments.
- The four Runeforged Elemental Enchantments are mutually exclusive; one weapon can carry only one of them.
- Cursed equipment cannot use the ordinary enchanting process.

## Elemental Affix Conflicts

When the Enchanting Table or Anvil tries to add an Enchantment to a weapon that already has Affixes, the following opposing relationships filter or reject that Enchantment application:

| Enchantment Side | Conflicting Weapon-Affix Side |
| --- | --- |
| Fire; vanilla Fire Aspect; vanilla Flame | Frost flat damage, Frost Compound Damage, Physical as Frost |
| Low Temperature | Fire flat damage, Fire Compound Damage, Physical as Fire |
| Lightning | Holy flat damage, Holy Compound Damage, Physical as Holy |
| Holy | Lightning flat damage, Lightning Compound Damage, Physical as Lightning |

Matching elements can coexist. For example, existing Fire flat damage does not block Fire; existing Frost-side Affixes do.

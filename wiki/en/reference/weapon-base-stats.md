# Weapon Base Stats

This page covers the seven standard material Weapon Families—Sword, Axe, Spear, Dagger, Rapier, Greatsword, and Scythe—before Quality, Affixes, Transmutation, Variants, Enchantments, or other Runeforged modifiers. Bows, Crossbows, Tridents, and Maces retain their own vanilla base stats and are outside this material-family matrix.

Each cell uses `Attack Damage / Attacks per Second / Durability`. Attack Damage is the complete base value shown by the item. More attacks per second means less time is required for a fully charged attack.

## Base Stats by Material

| Material | Sword | Axe | Spear | Dagger | Rapier | Greatsword | Scythe |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Wood | `4 / 1.60 / 59` | `7 / 0.80 / 59` | `1 / 1.54 / 59` | `3 / 2.00 / 44` | `4 / 1.50 / 59` | `10 / 0.60 / 59` | `4 / 1.10 / 59` |
| Stone | `5 / 1.60 / 131` | `9 / 0.80 / 131` | `2 / 1.33 / 131` | `3 / 2.20 / 98` | `5 / 1.50 / 131` | `11 / 0.60 / 131` | `5 / 1.10 / 131` |
| Copper | `5 / 1.60 / 190` | `9 / 0.80 / 190` | `2 / 1.18 / 190` | `4 / 2.20 / 143` | `5 / 1.50 / 190` | `12 / 0.60 / 190` | `6 / 1.10 / 190` |
| Iron | `6 / 1.60 / 250` | `9 / 0.90 / 250` | `3 / 1.05 / 250` | `4 / 2.30 / 188` | `6 / 1.50 / 250` | `12 / 0.70 / 250` | `6 / 1.20 / 250` |
| Gold | `4 / 1.60 / 32` | `7 / 1.00 / 32` | `1 / 1.05 / 32` | `3 / 2.20 / 24` | `4 / 1.50 / 32` | `10 / 0.60 / 32` | `4 / 1.10 / 32` |
| Diamond | `7 / 1.60 / 1561` | `9 / 1.00 / 1561` | `4 / 0.95 / 1561` | `4 / 2.40 / 1171` | `7 / 1.50 / 1561` | `12 / 0.80 / 1561` | `7 / 1.20 / 1561` |
| Netherite | `8 / 1.60 / 2031` | `10 / 1.00 / 2031` | `5 / 0.87 / 2031` | `5 / 2.40 / 1523` | `8 / 1.50 / 2031` | `14 / 0.80 / 2031` | `8 / 1.20 / 2031` |

Dagger base durability is `75%` of the material's standard durability, rounded to the nearest integer. The other six families use standard material durability.

Spears use individual attack durations. Their attacks-per-second values are `1 / attack duration`, displayed to two decimal places.

## Flat-Damage Coefficients

The flat-damage coefficient applies only to Physical/Elemental flat-damage Affixes and the flat portion of Compound Damage. It does not change percentage damage, the percentage portion of Compound Damage, Tier, or Affix count, and it does not scale Elemental Enchantment damage or fixed flat damage supplied directly by a Variant.

| Weapon Family | Physical Coefficient | Elemental Coefficient |
| --- | ---: | ---: |
| Sword | `1.00` | `1.00` |
| Axe | `1.25` | `1.25` |
| Spear | `0.80` | `0.80` |
| Dagger | `0.80` | `0.80` |
| Rapier | `1.00` | `1.00` |
| Greatsword | `1.40` | `1.40` |
| Scythe | `1.25` | `1.00` |
| Other affixable weapons | `1.00` | `1.00` |

Flat-damage ranges in the Affix table are base values at a `1.00` coefficient. Item display and combat use:

`Actual Flat Damage = Base Affix Flat Damage × Final Flat-Damage Coefficient`

A Special Weapon Variant directly modifies its family's coefficient:

`Final Flat-Damage Coefficient = Family Base Coefficient + Variant Coefficient Adjustment`

For example, Hand Axe starts from the Axe coefficient of `1.25` and applies `-0.05`, producing a final Physical and Elemental coefficient of `1.20`. Short Scythe is a special override: its Physical coefficient is fixed at `1.00` instead of adding an adjustment to the Scythe's `1.25`.

See [Special Weapon Variants](../equipment/special-weapon-variants.md) for every Variant adjustment.

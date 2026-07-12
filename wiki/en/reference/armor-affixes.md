# Armor Affixes

This page lists armor affixes available from ordinary equipment generation and regular affix forging. Slot labels are strict: Movement Speed appears only on Boots, for example.

## Damage-Reduction Rules

- Dodge is checked before damage; a success completely negates that melee or projectile hit.
- Armor and Armor Toughness are applied first, enchantment protection next, and percentage reduction affixes last.
- Armor is capped at `50`. The first `30` points use the Armor/Toughness formula; points above 30 provide additional reduction. The actual percentage depends on hit size and Toughness.
- Except for the fixed Legendary affix, all applicable reductions add together: All Damage Reduction, damage-category reduction, chestplate Physical/Elemental reduction, and one active Shelter.
- Fixed Legendary All Damage Reduction is independent: `10%` per ordinary Legendary armor piece or `15%` per Mythic piece, summed with an `80%` cap.
- `Combined reduction = 1 - (1 - additive reduction) × (1 - Legendary reduction)`.
- The complete armor-affix stage can remove at most `80%` of the damage entering it, leaving at least `20%`.
- Dodge applies only to melee and projectile damage and does not affect sources that bypass armor affixes.
- Debuff Duration Resistance linearly shortens negative effects. Slow Resistance reduces the movement penalty from Slowness rather than granting immunity.

Example: if 100 damage remains after Armor and enchantments, additive reduction is 40%, and Legendary reduction is 20%, the result is `100 × 0.60 × 0.80 = 48`, or 52% combined reduction.

## General Equipment and Armor Affixes

| Display name | Eligible | T4 | T3 | T2 | T1 |
| --- | --- | --- | --- | --- | --- |
| Extra Durability | All equipment | `+50%–100%` | `+100%–200%` | `+200%–500%` | — |
| Max Health | Armor | `+1.0–1.5` | `+1.5–2.0` | `+2.0–2.5` | `+2.5–4.0` |
| Armor | Armor | `+0.5–1.0` | `+1.0–1.5` | `+1.5–2.0` | `+2.0–3.0` |
| Armor Toughness | Armor | — | `+0.50–0.75` | `+0.75–1.25` | `+1.25–2.00` |
| Melee Damage Reduction | Armor | `+6%–8%` | `+8%–10%` | `+10%–12%` | `+12%–16%` |
| Projectile Damage Reduction | Armor | `+8%–12%` | `+12%–16%` | `+16%–24%` | `+24%–32%` |
| Explosion Damage Reduction | Armor | `+8%–12%` | `+12%–16%` | `+16%–24%` | `+24%–32%` |
| Fire Damage Reduction | Armor | `+8%–12%` | `+12%–16%` | `+16%–24%` | `+24%–32%` |
| Shelter of the Sun | Armor | — | `+6%–10%` | `+10%–14%` | `+14%–20%` |
| Shelter of Shadows | Armor | — | `+6%–10%` | `+10%–14%` | `+14%–20%` |
| Shelter of Storms | Armor | — | `+8%–12%` | `+12%–16%` | `+16%–24%` |
| Shelter of Otherworlds | Armor | — | `+8%–12%` | `+12%–16%` | `+16%–24%` |
| Knockback Resistance | Armor | `+12%–18%` | `+18%–24%` | `+24%–36%` | `+36%–50%` |

## Helmet

| Display name | T2 | T1 | Scope |
| --- | --- | --- | --- |
| Elemental Damage | `+16%–24%` | `+24%–32%` | Melee, ranged, and Weapon Skills |
| Physical Damage | `+10%–14%` | `+14%–20%` | Melee, ranged, and Weapon Skills |
| Suffocation Damage Reduction | `+24%–36%` | `+36%–54%` | In-wall suffocation and drowning |

## Chestplate

| Display name | T3 | T2 | T1 |
| --- | --- | --- | --- |
| Physical Damage Reduction | `+5%–7.5%` | `+7.5%–10%` | `+10%–15%` |
| Elemental Damage Reduction | `+5%–7.5%` | `+7.5%–10%` | `+10%–15%` |
| Debuff Duration Resistance | `+12%–16%` | `+16%–24%` | `+24%–40%` |

## Leggings

| Display name | T2 | T1 | Scope |
| --- | --- | --- | --- |
| Dodge Chance | `+6%–8%` | `+8%–12%` | Melee and projectile damage |
| Slow Resistance | `+25%–35%` | `+35%–50%` | Slowness movement penalty |

## Boots

| Display name | T3 | T2 | T1 |
| --- | --- | --- | --- |
| Movement Speed | `+6%–8%` | `+8%–12%` | `+12%–20%` |

Dodge Chance appears only on Leggings. Boots cannot roll Dodge Chance.

## Conflicts

| Group | Rule |
| --- | --- |
| Armor reduction | Melee, Projectile, Explosion, Fire, chestplate Physical, chestplate Elemental, and helmet Suffocation reduction conflict |
| Shelter | Sun, Shadows, Storms, and Otherworlds conflict |
| Helmet output | Helmet Elemental and Physical Damage conflict |

## Shelter Conditions

- Shelter of the Sun: Overworld daytime.
- Shelter of Shadows: Overworld night.
- Shelter of Storms: in water, or Overworld rain in a biome with precipitation.
- Shelter of Otherworlds: any non-Overworld dimension.

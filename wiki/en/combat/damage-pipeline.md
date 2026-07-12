# Damage Calculation

A weapon hit can contain Physical, Fire, Frost, Lightning, and Holy Damage. Elemental flat damage and Physical conversion enter the full weapon-damage process; vanilla enchantment damage is added near the end and does not benefit from most weapon multipliers.

## Weapon Damage Composition

### Physical Base

`Total Physical = (Base weapon Physical + flat Physical Damage) × (1 + Physical Damage %)`

For a vanilla falling critical, base weapon damage is first restored to its non-critical value; the vanilla `1.5` multiplier is applied later with the other multipliers.

### Physical Conversion

All Physical-to-element conversion percentages are added together, capped at `100%`. Conversion affects the Physical total above but not vanilla enchantment damage.

### Elemental Damage

Each element is calculated separately:

`Element = (flat elemental damage + converted Physical) × (1 + Elemental Damage % + element-specific bonus)`

## Weapon Damage Multipliers

Remaining Physical and all four elemental buckets share the following multipliers:

| Multiplier | Rule |
| --- | --- |
| Slayer and Blessing | The highest applicable regular Slayer is added to all active Blessings |
| Giant-variant Slayer | Independent multiplier against Giant variants: Giant Slayer `×2.0`; matching Undead and Human Slayer each `×1.5` |
| All Damage | Ordinary All Damage values add together into one multiplier |
| Legendary All Damage | Fixed Legendary weapon bonus is independent |
| Unique All Damage | Unique All Damage is independent |
| Runeforged Critical Strike | Randomly triggered by Critical Strike Chance; base bonus is `50%` plus Critical Strike Damage |
| Single-Wield Damage | Active with an empty offhand |
| Leap Attack Damage | Active when the hit meets vanilla falling-critical conditions |
| Dash Attack Damage | Active on a sprint attack |
| Vanilla critical | `×1.5` when vanilla falling-critical conditions are met |

These rows multiply one another. Slayer/Blessing `40%`, All Damage `20%`, and a Runeforged Critical Strike `50%` produce `1.40 × 1.20 × 1.50`, not one additive `110%` bonus.

Runeforged Critical Strikes and vanilla falling criticals are independent. Leap Attack Damage checks the vanilla falling critical and does not activate from Critical Strike Chance.

## Curses and Enchantment Damage

Cursed Physical and Elemental Damage penalties multiply their matching buckets after the weapon multipliers above.

Vanilla enchantment damage and enchantment-style elemental additions are then added as flat damage. They do not benefit from Physical/Elemental %, Slayer, Blessing, All Damage, Runeforged Critical Strike, Single-Wield, Leap, or Dash multipliers.

## Defense

### Physical Damage

1. Full target Armor and Armor Toughness are applied; Armor Penetration lowers the Armor used for this hit.
2. Enchantment protection and other magic protection are applied.
3. Armor-affix percentage reductions and Legendary All Damage Reduction are applied.

Armor is capped at `50`. The first `30` points use the Armor and Armor Toughness formula, while points above 30 provide additional reduction. The actual percentage depends on hit size and Armor Toughness.

### Elemental Damage

1. `75%` of target Armor and `75%` of Armor Toughness are applied; Armor Penetration also lowers this Armor.
2. The matching elemental resistance is applied. Resistance before penetration is clamped to `-100%–95%`, then Elemental Resistance Penetration is subtracted.
3. Applicable armor-affix reductions are applied.

Positive resistance reduces damage; negative resistance increases it. See [Elements, Resistances & Status Effects](elements-and-resistances.md).

### Armor-Affix Reduction

Applicable ordinary reductions add together: All Damage Reduction, Melee/Projectile/Explosion/Fire reduction, chestplate Physical/Elemental reduction, and one active Shelter. Legendary fixed All Damage Reduction is an independent multiplier:

`Combined reduction = 1 - (1 - additive reduction) × (1 - Legendary reduction)`

Legendary reduction itself is capped at `80%`, and the entire armor-affix stage can remove at most `80%` of the damage entering that stage. See [Armor Affixes](../reference/armor-affixes.md).

## On-Hit Elemental Effects and Armor Break

Fire, Frost, Lightning, Holy effects and Physical armor-break thresholds use the corresponding raw damage bucket before Armor and resistance.

Physical hits apply 4-second Armor Break. Raw Physical Damage of `5 / 10 / 40` adds `5% / 10% / 25%`, stacking up to `50%`. It acts alongside Slice's Armor reduction. Monster-sourced Physical Armor Break does not affect players.

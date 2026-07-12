# Rune-Cursed Weapons

Rune-Cursed Weapons are crafted from a blank weapon and a specified currency. Each archetype has fixed abilities plus additional random affixes.

## Crafting

The five standard routes use one blank weapon in the center and eight identical Rune Stones around it. The three special routes use one blank weapon in the center and four identical gems above, below, left, and right; all corners stay empty.

| Currency | Archetype | Pattern |
| --- | --- | --- |
| Shaping Stone | Foundation | 8 around center |
| Reinforcement Stone | Military | 8 around center |
| Reforging Stone | Molten | 8 around center |
| Stripping Stone | Purification | 8 around center |
| Tempering Stone | Resonance | 8 around center |
| Alien Gem | Bloodthirst | 4 cardinal slots |
| Sealed Gem | Ancient | 4 cardinal slots |
| Infusion Gem | Nature | 4 cardinal slots |

## Blank Weapon

The center item must be an affixable Common weapon with no enchantments or stored enchantments. A Common weapon carrying only a Sealed fixed affix is still blank. Full durability is not required; the result is fully repaired.

## Eligible Weapon Families

| Archetype | Eligible weapons |
| --- | --- |
| Foundation | Sword, Axe, Greatsword, Rapier, Spear |
| Military | Sword, Rapier, Dagger, Spear |
| Molten | Axe, Greatsword, Scythe, Spear |
| Purification | Sword, Rapier, Dagger, Scythe, Greatsword |
| Resonance | Sword, Rapier, Dagger, Scythe, Greatsword, Axe |
| Bloodthirst | Dagger, Axe, Scythe, Spear |
| Ancient | Sword, Axe, Greatsword, Scythe, Spear |
| Nature | Sword, Dagger, Rapier, Scythe, Spear |

## Result Structure

Every result is Cursed and contains fixed-value affixes, fixed-Tier affixes whose values roll inside that Tier, and one additional random T3/T2/T1 affix. Archetypes may also add a Sealed or Infusion Affix.

## Foundation

Fixed values:

- Physical Damage `+2`
- Physical Damage `+10%`

Fixed Tiers:

- Physical Damage T2
- Physical Damage % T3
- Max Durability T3

## Military

Fixed values:

- Single-Wield Damage `+20%`
- Dash Attack Damage `+20%`

Fixed Tiers:

- one T2 main damage affix chosen from Physical, Fire, Frost, Lightning, or Holy Damage;
- Physical Damage % T3 if Physical was selected, otherwise Elemental Damage % T3;
- Critical Strike Chance T3.

## Molten

Fixed values:

- `50%` Physical converted to Fire
- Attack Range `+0.5`

Fixed Tiers:

- Fire Damage T2
- Elemental Damage % T3
- Fire Compound Damage T3
- Knockback Distance T3

## Purification

Fixed values:

- `50%` Physical converted to Holy
- On-Kill Heal `+2`

Fixed Tiers:

- Holy Damage T2
- Elemental Damage % T3
- Undead Slayer T3
- Blessing of the Sun T3

## Resonance

Fixed values:

- Elemental Damage `+20%`
- one of its two selected elements receives `20%` Physical conversion

Fixed Tiers:

- one T3 elemental flat-damage affix;
- a second T3 flat-damage affix from the opposite group: Fire/Frost pairs with Lightning/Holy and vice versa;
- the other selected element receives Physical conversion T3;
- Elemental Damage % T2.

## Bloodthirst

Fixed values:

- Critical Strike Chance `+25%`
- Critical Strike Damage `+50%`

Fixed Tiers:

- one random elemental flat-damage affix T3
- Critical Strike Chance T2
- one random Undead/Human/Giant Slayer T3
- Attack Speed T3

A new Bloodthirst weapon has two remaining Alienations. Each successful Alien Gem use consumes one, and the remaining count is shown on the item.

## Ancient

The weapon chooses either Frost or Lightning as its main route.

Fixed values:

- `50%` Physical converted to the main element
- main-element Damage `+25%`

Fixed Tiers:

- main-element Compound Damage T2
- main-element flat Damage T3
- Elemental Resistance Penetration T3
- Armor Penetration T3

It also gains one extra Sealed flat-damage affix matching the main element at T2.

## Nature

Fixed values:

- `50%` Physical converts to the active Nature element; the weapon cycles Fire → Frost → Lightning after attacking
- Attack Speed `+15%`

Fixed Tiers:

- Elemental Damage % T2
- Physical Damage T3
- Physical Compound Damage T3
- Attack Range T3

It also gains one T2 Infusion Affix. The affix type is selected once, its value is rolled three times, and the best is kept. Nature weapons can continue accumulating Infusion, reroll at `100%`, or use an Infusion Gem directly.

## Related Systems

- Alienation preserves the Rune archetype.
- Rune-Cursed Weapons cannot use the ordinary enchanting process.
- Bloodthirst supports at most two Alienations; Nature supports repeatable Infusion.
- Some generated blank chest or fishing weapons have a `1%` chance to become Rune-Cursed directly.

Tier ranges are listed under [Weapon Affixes](../reference/weapon-affixes.md).

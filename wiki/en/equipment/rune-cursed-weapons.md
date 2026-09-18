# Rune-Cursed Weapons

Rune-Cursed Weapons are crafted from a blank weapon and a specified currency. Each archetype has fixed abilities plus additional random affixes.

## Crafting

Rune-Cursed Weapons use a `3×3` recipe. The two route layouts are:

| Route | Eligible currency | Center slot | Other slots |
| --- | --- | --- | --- |
| Five standard routes | Shaping, Reinforcement, Reforging, Stripping, or Tempering Stone | One blank weapon | Eight identical Rune Stones in the outer ring |
| Three special routes | Alien, Sealed, or Infusion Gem | One blank weapon | Four identical gems in the cardinal slots; corners empty |

Every route also accepts the matching Celestial currency in the same layout. All currency items in one recipe must be either ordinary or Celestial; the two versions cannot be mixed.

## Blank Weapon

The center item must be an affixable Common weapon with no enchantments or stored enchantments. A Common weapon carrying only a Sealed fixed affix is still blank. A weapon carrying an [Infused Gem](infused-gems.md) is not eligible. Full durability is not required; the result is fully repaired.

## Eligible Weapon Families

| Archetype | Currency | Eligible weapons |
| --- | --- | --- |
| Foundation | Shaping Stone | Sword, Axe, Greatsword, Rapier, Spear |
| Military | Reinforcement Stone | Sword, Rapier, Dagger, Spear |
| Molten | Reforging Stone | Axe, Greatsword, Scythe, Spear |
| Purification | Stripping Stone | Sword, Rapier, Dagger, Scythe, Greatsword |
| Resonance | Tempering Stone | Sword, Rapier, Dagger, Scythe, Greatsword, Axe |
| Bloodthirst | Alien Gem | Dagger, Axe, Scythe, Spear |
| Ancient | Sealed Gem | Sword, Axe, Greatsword, Scythe, Spear |
| Nature | Infusion Gem | Sword, Dagger, Rapier, Scythe, Spear |

## Result Structure

Every result is Cursed and contains fixed-value affixes, fixed-Tier affixes whose values roll inside that Tier, and additional random affixes. Ordinary recipes add one random T3/T2/T1 affix. Celestial Foundation and Military recipes add two random affixes in total; the other six Celestial routes add one. Archetypes may also add a Sealed or Infusion Affix.

Celestial results retain Cursed quality and the Rune overlay, but use Celestial glint and a Celestial name prefix.

## Archetype Details

### Foundation

Fixed values:

- Physical Damage `+2`
- Physical Damage `+10%`

Fixed Tiers:

- Physical Damage T2
- Physical Damage % T3
- Max Durability T3

**Celestial Foundation:** Physical Damage becomes T1, Physical Damage % becomes T1, and Max Durability becomes T2. Its original random affix resolves as T3→T2, T2→T1, or an eligible T1→fixed regular T0, while an existing T0 remains T0. A second random affix is then rolled at its normal T3/T2/T1 result and is not converted again. The fixed `+2` Physical Damage and `+10%` Physical Damage values do not change.

### Military

Fixed values:

- Single-Wield Damage `+20%`
- Dash Attack Damage `+20%`

Fixed Tiers:

- one T2 main damage affix chosen from Physical, Fire, Frost, Lightning, or Holy Damage;
- Physical Damage % T3 if Physical was selected, otherwise Elemental Damage % T3;
- Critical Strike Chance T3.

**Celestial Military:** the selected main damage becomes T1, its matching Physical or Elemental Damage % becomes T2, and Critical Strike Chance becomes T2. Its original random affix resolves as T3→T2, T2→T1, or an eligible T1→fixed regular T0, while an existing T0 remains T0. A second random affix is then rolled normally and is not converted again. Single-Wield Damage and Dash Attack Damage remain `+20%`.

### Molten

Fixed values:

- `50%` Physical converted to Fire
- Attack Range `+0.5`

Fixed Tiers:

- Fire Damage T2
- Elemental Damage % T3
- Fire Compound Damage T3
- Knockback Distance T3

**Celestial Molten:** Fire Damage becomes T1, Elemental Damage % becomes T2, Fire Compound Damage becomes T1, and Knockback Distance becomes T2. Its random affix resolves as T3→T2, T2→T1, or an eligible T1→fixed regular T0, while an existing T0 remains T0. The `50%` Physical-to-Fire conversion and `+0.5` Attack Range do not change.

### Purification

Fixed values:

- `50%` Physical converted to Holy
- On-Kill Heal `+2`

Fixed Tiers:

- Holy Damage T2
- Elemental Damage % T3
- Undead Slayer T3
- Blessing of the Sun T3

**Celestial Purification:** Holy Damage becomes T1, Elemental Damage % becomes T2, Undead Slayer becomes T2, and Blessing of the Sun becomes T1. Its random affix resolves as T3→T2, T2→T1, or an eligible T1→fixed regular T0, while an existing T0 remains T0. The `50%` Physical-to-Holy conversion and `+2` On-Kill Heal do not change.

### Resonance

Fixed values:

- Elemental Damage `+20%`
- one of its two selected elements receives `20%` Physical conversion

Fixed Tiers:

- one T3 elemental flat-damage affix;
- a second T3 flat-damage affix from the opposite group: Fire/Frost pairs with Lightning/Holy and vice versa;
- the other selected element receives Physical conversion T3;
- Elemental Damage % T2.

**Celestial Resonance:** both selected elemental flat-damage affixes become T2, the selected conversion becomes T2, and Elemental Damage % becomes T1. Its random affix resolves as T3→T2, T2→T1, or an eligible T1→fixed regular T0, while an existing T0 remains T0. The fixed `+20%` Elemental Damage and `20%` conversion do not change.

### Bloodthirst

Fixed values:

- Critical Strike Chance `+25%`
- Critical Strike Damage `+50%`

Fixed Tiers:

- one random elemental flat-damage affix T3
- Critical Strike Chance T2
- one random Undead/Human/Giant Slayer T3
- Attack Speed T3

**Celestial Bloodthirst:** the elemental flat-damage affix becomes T2, Critical Strike Chance becomes T1, the selected Slayer becomes T2, and Attack Speed becomes T2. Its random affix resolves as T3→T2, T2→T1, or an eligible T1→fixed regular T0, while an existing T0 remains T0. The fixed Critical Strike Chance, Critical Strike Damage, and two remaining Alienations do not change.

A new Bloodthirst weapon has two remaining Alienations. Each successful Alien Gem use consumes one, and the remaining count is shown on the item.

### Ancient

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

**Celestial Ancient:** the main-element Compound Damage remains T2, while the main-element flat Damage, Elemental Resistance Penetration, and Armor Penetration become T2. Its random affix resolves as T3→T2, T2→T1, or an eligible T1→fixed regular T0, while an existing T0 remains T0. The extra Sealed T2 flat-damage affix and all fixed values do not change.

### Nature

Fixed values:

- `50%` Physical converts to the active Nature element; the weapon cycles Fire → Frost → Lightning after attacking
- Attack Speed `+15%`

Fixed Tiers:

- Elemental Damage % T2
- Physical Damage T3
- Physical Compound Damage T3
- Attack Range T3

It also gains one T2 Infusion Affix. The affix type is selected once, its value is rolled three times, and the best is kept. Nature weapons can continue accumulating Infusion, reroll at `100%`, or use an Infusion Gem directly.

**Celestial Nature:** Elemental Damage % becomes T1, Physical Damage becomes T2, Physical Compound Damage becomes T2, and Attack Range becomes T2 with a default `+0.30–0.50` range. Its random affix resolves as T3→T2, T2→T1, or an eligible T1→fixed regular T0, while an existing T0 remains T0. The T2 Infusion Affix, element cycle, conversion, and fixed Attack Speed do not change.

## Related Systems

- Alienation preserves the Rune archetype.
- Rune-Cursed Weapons cannot use the ordinary enchanting process.
- Ordinary and Celestial Rune-Cursed recipes cannot use a gem-modified base weapon.
- Bloodthirst supports at most two Alienations; Nature supports repeatable Infusion.
- Some generated blank chest or fishing weapons have a `1%` chance to become Rune-Cursed directly.

## Related Data

- [Weapon Affixes](../reference/weapon-affixes.md) lists the default ranges for the corresponding affixes.
- Server configuration may change affix values.

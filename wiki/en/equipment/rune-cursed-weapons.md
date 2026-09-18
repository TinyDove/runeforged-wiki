# Rune-Cursed Weapons

Rune-Cursed Weapons are crafted from a blank weapon and a specified currency. Each archetype has fixed abilities plus additional random affixes.

## Crafting

Rune-Cursed Weapons use a `3×3` recipe. The two route layouts are:

| Route | Eligible currency | Center slot | Other slots |
| --- | --- | --- | --- |
| Five standard routes | Shaping, Reinforcement, Reforging, Stripping, or Tempering Stone | One blank weapon | Eight identical Rune Stones in the outer ring |
| Three special routes | Alien, Sealed, or Infusion Gem | One blank weapon | Four identical gems in the cardinal slots; corners empty |

Every route also accepts the matching Celestial currency in the same layout. All currency items in one recipe must be either ordinary or Celestial; the two versions cannot be mixed.

### Celestial Rune-Cursed Weapons

Celestial Rune-Cursed Weapons use the matching Celestial currency. The result has Cursed quality, Celestial glint, and a Celestial name prefix. Each archetype uses the Celestial fixed parameters listed below.

Celestial Foundation and Military weapons have two random affixes; the other Celestial archetypes have one. Every random affix is generated from T3 / T2 / T1.

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

## Archetype Parameters

Fixed Tier affixes roll a value inside the listed Tier.

### Foundation

| Parameter | Ordinary | Celestial |
| --- | --- | --- |
| Fixed values | Physical Damage `+2`; Physical Damage `+10%` | Physical Damage `+2`; Physical Damage `+10%` |
| Fixed Tiers | Physical Damage T2; Physical Damage % T3; Max Durability T3 | Physical Damage T1; Physical Damage % T1; Max Durability T2 |
| Random affixes | One T3 / T2 / T1 | Two T3 / T2 / T1 |

### Military

Main damage is selected from Physical, Fire, Frost, Lightning, or Holy Damage. The Physical route uses Physical Damage %, while elemental routes use Elemental Damage %.

| Parameter | Ordinary | Celestial |
| --- | --- | --- |
| Fixed values | Single-Wield Damage `+20%`; Dash Attack Damage `+20%` | Single-Wield Damage `+20%`; Dash Attack Damage `+20%` |
| Fixed Tiers | Main Damage T2; matching Damage % T3; Critical Strike Chance T3 | Main Damage T1; matching Damage % T2; Critical Strike Chance T2 |
| Random affixes | One T3 / T2 / T1 | Two T3 / T2 / T1 |

### Molten

| Parameter | Ordinary | Celestial |
| --- | --- | --- |
| Fixed values | `50%` Physical converted to Fire; Attack Range `+0.5` | `50%` Physical converted to Fire; Attack Range `+0.5` |
| Fixed Tiers | Fire Damage T2; Elemental Damage % T3; Fire Compound Damage T3; Knockback Distance T3 | Fire Damage T1; Elemental Damage % T2; Fire Compound Damage T1; Knockback Distance T2 |
| Random affixes | One T3 / T2 / T1 | One T3 / T2 / T1 |

### Purification

| Parameter | Ordinary | Celestial |
| --- | --- | --- |
| Fixed values | `50%` Physical converted to Holy; On-Kill Heal `+2` | `50%` Physical converted to Holy; On-Kill Heal `+2` |
| Fixed Tiers | Holy Damage T2; Elemental Damage % T3; Undead Slayer T3; Blessing of the Sun T3 | Holy Damage T1; Elemental Damage % T2; Undead Slayer T2; Blessing of the Sun T1 |
| Random affixes | One T3 / T2 / T1 | One T3 / T2 / T1 |

### Resonance

The two flat-damage elements come from opposite groups: Fire/Frost and Lightning/Holy. One receives fixed `20%` Physical conversion; the other receives a Tiered conversion.

| Parameter | Ordinary | Celestial |
| --- | --- | --- |
| Fixed values | Elemental Damage `+20%`; one Physical-to-element conversion `20%` | Elemental Damage `+20%`; one Physical-to-element conversion `20%` |
| Fixed Tiers | Two elemental flat-damage affixes T3; other conversion T3; Elemental Damage % T2 | Two elemental flat-damage affixes T2; other conversion T2; Elemental Damage % T1 |
| Random affixes | One T3 / T2 / T1 | One T3 / T2 / T1 |

### Bloodthirst

| Parameter | Ordinary | Celestial |
| --- | --- | --- |
| Fixed values | Critical Strike Chance `+25%`; Critical Strike Damage `+50%` | Critical Strike Chance `+25%`; Critical Strike Damage `+50%` |
| Fixed Tiers | Random elemental flat damage T3; Critical Strike Chance T2; random Undead/Human/Giant Slayer T3; Attack Speed T3 | Random elemental flat damage T2; Critical Strike Chance T1; random Undead/Human/Giant Slayer T2; Attack Speed T2 |
| Random affixes | One T3 / T2 / T1 | One T3 / T2 / T1 |
| Alienations | 2 | 2 |

Each successful Alienation consumes one use. The remaining count appears on the item.

### Ancient

The main element is selected from Frost and Lightning.

| Parameter | Ordinary | Celestial |
| --- | --- | --- |
| Fixed values | `50%` Physical converted to the main element; main-element Damage `+25%` | `50%` Physical converted to the main element; main-element Damage `+25%` |
| Fixed Tiers | Main-element Compound Damage T2; main-element flat Damage T3; Elemental Resistance Penetration T3; Armor Penetration T3 | Main-element Compound Damage T2; main-element flat Damage T2; Elemental Resistance Penetration T2; Armor Penetration T2 |
| Random affixes | One T3 / T2 / T1 | One T3 / T2 / T1 |
| Sealed affix | One maximum-roll main-element flat Damage T2 | One maximum-roll main-element flat Damage T2 |

### Nature

The active element cycles Fire → Frost → Lightning after each attack.

| Parameter | Ordinary | Celestial |
| --- | --- | --- |
| Fixed values | `50%` Physical converted to the active element; Attack Speed `+15%` | `50%` Physical converted to the active element; Attack Speed `+15%` |
| Fixed Tiers | Elemental Damage % T2; Physical Damage T3; Physical Compound Damage T3; Attack Range T3 | Elemental Damage % T1; Physical Damage T2; Physical Compound Damage T2; Attack Range T2 |
| Random affixes | One T3 / T2 / T1 | One T3 / T2 / T1 |
| Infusion affix | One T2; type selected once, value rolled three times with the best kept | One T2; type selected once, value rolled three times with the best kept |

Nature weapons can continue accumulating Infusion, reroll at `100%`, or use an Infusion Gem directly.

## Related Systems

- Alienation preserves the Rune archetype.
- Rune-Cursed Weapons cannot use the ordinary enchanting process.
- Ordinary and Celestial Rune-Cursed recipes cannot use a gem-modified base weapon.
- Bloodthirst supports at most two Alienations; Nature supports repeatable Infusion.
- Some generated blank chest or fishing weapons have a `1%` chance to become Rune-Cursed directly.

## Related Data

- [Weapon Affixes](../reference/weapon-affixes.md) lists the default ranges for the corresponding affixes.
- Server configuration may change affix values.

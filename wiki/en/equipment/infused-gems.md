# Infused Gems

Infused Obsidian, Infused Amethyst, Infused Lapis Lazuli, and Infused Ruby modify the regular-affix area of weapons and armor. They are separate from the existing **Infusion Gem**, which controls Infusion Value and Infusion Affixes.

## Crafting and Use

Each Infused Gem uses a shaped `3×3` recipe: place one ordinary Infusion Gem in the center and eight matching materials around it.

| Result | Outer material |
| --- | --- |
| Infused Obsidian | Obsidian |
| Infused Amethyst | Amethyst Shard |
| Infused Lapis Lazuli | Lapis Lazuli |
| Infused Ruby | Redstone Dust |

Apply one Infused Gem together with one eligible item in a crafting grid. The item must be an affixable Common or Magic weapon or armor. One item can carry only one Infused Gem, and it cannot be replaced directly.

The item name gains an Obsidian, Amethyst, Lapis Lazuli, or Ruby prefix without the word “Infused.” Existing custom names are preserved.

## Effects and Capacity

Every effect below applies only to regular main affixes. Legendary, Sealed, Infusion, curse-area, negative, fixed Rune, and other special affixes do not count toward the modified capacity and do not receive the value modifier.

| Gem | Regular-affix effect | Rare-or-higher regular capacity |
| --- | --- | ---: |
| Infused Obsidian | All regular-affix values ×`0.85` | 6 |
| Infused Amethyst | The top regular affix value ×`2` | 4 |
| Infused Lapis Lazuli | For non-T0 affixes, raises the maximum by 20% while preserving the minimum and stored roll | 4 |
| Infused Ruby | Regular flat damage and damage-reduction values ×`1.5`; on compound damage, only the flat part is increased | 4 |

Common equipment still has no regular affix, and Magic equipment still has a limit of three. The capacity change begins at Rare quality. Four regular affixes still promote Magic equipment to Rare.

Infused Lapis Lazuli resolves a value as:

```text
minimum + (maximum × 1.2 - minimum) × stored roll
```

It does not affect an affix that was already T0 before the gem modifier. The other three gems can affect regular T0 affixes. Masterwork multiplies the value after the Infused Gem modifier is resolved.

## Other Equipment Systems

- Applying an Infused Gem removes an existing Weapon Transmutation. A gem-modified weapon cannot receive another Transmutation or be used as the base for a Rune-Cursed recipe.
- Ascension and Alienation remain available. Their regular-affix generation respects the modified capacity.
- Reforging removes the Infused Gem. The item can then receive another gem or a Transmutation.
- Repair preserves the gem. Two items carrying different Infused Gems cannot be combined for repair; matching gems, or one gem-modified and one unmodified item, are compatible.
- Natural Rune-Cursed equipment never receives an Infused Gem.

## Obtaining

The four gems share one reward pool and are equally likely whenever that pool succeeds.

- Hostile monsters: the pool starts at `0.12%` at level 20, reaches `0.20%` at level 50, and `0.24%` at the default global cap of 100 before other drop modifiers.
- Chests, fishing, and Elite bonus rewards include one pool entry alongside existing high-tier currency.
- Eligible naturally generated weapons and armor have a `1%` total chance to carry one of the four gems. This is decided once before regular affixes are generated.
- Villagers and wandering traders do not sell the four finished gems directly.

See [Monster Drops](../obtaining/monster-drops.md), [Chests & Trades](../obtaining/chests-and-trades.md), [Fishing](../obtaining/fishing.md), and [Elite Monsters](../monsters/elites.md) for source-specific tables.

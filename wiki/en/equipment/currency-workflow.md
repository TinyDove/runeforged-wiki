# Equipment Currency

Equipment currency is normally used in the player crafting grid or a crafting table. Unless stated otherwise, place exactly one affixable item and one currency item anywhere in the grid. Random outcomes are finalized when the result is taken.

## Base Currency Recipes

These recipes use a crafting table. Counts are totals for the complete recipe. Cobblestone in Shaping Stone, Reinforcement Stone, and Edict Stone recipes can also be replaced with Blackstone or Cobbled Deepslate.

| Currency | Required materials |
| --- | --- |
| Shaping Stone | 6 Cobblestone, 3 Copper Ingots |
| Reinforcement Stone | 6 Cobblestone, 2 Copper Ingots, 1 Iron Ingot |
| Tempering Stone | 6 Lapis Lazuli, 3 Gold Ingots |
| Reforging Stone | 6 Glass, 2 Iron Ingots, 1 Gold Ingot |
| Stripping Stone | 6 Redstone Dust, 3 Gold Ingots |
| Alien Gem | 6 Redstone Dust, 2 Gold Ingots, 1 Eye of Ender |
| Penance Stone | 6 Amethyst Shards, 2 Lapis Lazuli, 1 Diamond |
| Edict Stone | 6 Cobblestone, 2 Gold Ingots, 1 Diamond |
| Sealed Gem | 6 Redstone Dust, 2 Diamonds, 1 Eye of Ender |
| Infusion Gem | 6 Lapis Lazuli, 2 Gold Ingots, 1 Diamond |
| Ascension Stone | 4 Gold Ingots, 4 Diamonds, 1 Netherite Ingot |

## Quality and Regular-Affix Count

| Quality | Regular affixes |
| --- | ---: |
| Common | 0 |
| Magic | 1–3 |
| Rare | 4–5 |
| Legendary | 5, plus a Legendary Affix |

## Shaping Stone

Turns Common equipment with no regular affixes into Magic equipment and adds one random regular affix.

## Reinforcement Stone

Adds one random regular affix to Magic equipment with 1–2 regular affixes, up to three. Quality remains Magic.

## Tempering Stone

Adds one random regular affix to non-Cursed equipment below its regular-affix limit. At four affixes the item becomes Rare; the limit is five.

When a weapon first becomes Rare and still has no direct damage affix, the newly added affix is selected from weapon damage affixes.

## Reforging Stone

Clears Runeforged forging and repairs durability according to the number of removed regular affixes.

It cannot be used on Legendary equipment, any Cursed equipment (including Alien, Sealed, and Rune-Cursed), equipment carrying a Sealed Affix, or an item with no Runeforged equipment data. It clears quality, all mutable equipment affixes, and enchantments.

| Removed regular affixes | Maximum durability repaired |
| ---: | ---: |
| 1 | 15% |
| 2 | 30% |
| 3 | 45% |
| 4 | 75% |
| 5 or more | 100% |

At a Smithing Table, a Reforging Stone also has a separate use: combine it with target equipment and a higher-material blank weapon of the same family or armor of the same slot for [Equipment Material Upgrade](material-upgrade.md). Material Upgrade does not perform the clearing or repair operation described above.

## Stripping Stone

Removes one random regular affix. The item drops from Rare to Magic below four regular affixes. Removing its final regular affix clears mutable Runeforged properties, while Sealed Affixes remain.

## Penance Stone

Replaces one lowest-Tier regular affix. If several share the lowest Tier, one is selected randomly. The replacement is compatible with the item, and total affix count remains unchanged.

## Edict Stone

Rerolls the values of all regular affixes within their existing Tiers. Names, Tiers, count, quality, Legendary Affixes, and other special affixes remain unchanged.

## Ascension Stone

Turns Common, Magic, or Rare equipment Legendary, fills it to five regular affixes, and adds one T1 Legendary Affix. A Legendary weapon gains the fixed `10%` All Damage affix; Legendary armor gains fixed `10%` All Damage Reduction.

## Celestial Fragment

Rerolls the Legendary Affix on Legendary or Mythic equipment that already has one. A Mythic result remains maximum-value T0. Regular affixes, quality, the fixed Legendary bonus, Sealed Affixes, and other special effects remain unchanged.

## Sealed Gem

Turns eligible Rare equipment into Sealed Cursed equipment, or rerolls the curse area of eligible Cursed equipment.

Requirements:

- at least one regular affix;
- Rare equipment is eligible directly;
- Cursed equipment must be Normal Cursed or Sealed Cursed; Alien and Rune-Cursed equipment are ineligible.

Results:

- a Rare item becomes Sealed Cursed and preserves its regular affixes;
- the curse area gains 2–3 T3–T1 affixes: `75%` for two, `25%` for three;
- one negative curse is added;
- another use on Normal or Sealed Cursed equipment rerolls the entire curse area and negative curse.

A Celestial Sealed Gem always creates three curse-area affixes, at least one of which is T1, and rerolls one negative curse. Sealed Gems are also ingredients for Origin Transmutation and Ancient Rune-Cursed Weapons.

## Infusion Gem

Eligible non-Common equipment gains `25–100` Infusion Value while incomplete. At `100%`, an existing Infusion Affix can be replaced and progress is cleared. Normal Cursed equipment cannot reroll after receiving its first Infusion Affix; Nature Rune-Cursed Weapons can repeat the cycle. See [Infusion](infusion.md).

Infusion Gems are also ingredients for Triad Transmutation and Nature Rune-Cursed Weapons.

## Alien Gem

Turns equipment into Alien-Cursed equipment and applies several random changes. See [Alien Gem](alien-orb.md) for the full change pool, T0 affixes, and restrictions.

## Targeted Currency

Shaping Stones, Reinforcement Stones, Tempering Stones, and Ascension Stones can carry a specified affix. They use the same operation as the base currency, but the newly created affix is the one displayed on the currency.

Four copies of the same base currency can craft one targeted version. Non-crafted base currency can also become targeted:

| Source | Chance |
| --- | ---: |
| Ordinary drop | 5% |
| Fishing | 50% |

Some targeted Shaping, Reinforcement, and Tempering Stones also lock the affix Tier. Ascension Stones do not have a Sealed version.

## Celestial Currency

| Currency | Difference from the base version |
| --- | --- |
| Celestial Tempering Stone | Adds at least T1; has a `10%` chance to attempt an eligible regular T0 and falls back to T1 when none is available; targeted or Sealed versions follow their displayed rule |
| Celestial Stripping Stone | Removes the bottom regular affix in the displayed list |
| Celestial Alien Gem | Fills regular affixes by the Alienation rule, then makes `4–6` random-change rolls |
| Celestial Sealed Gem | Creates three curse-area affixes with at least one T1; a reroll rebuilds the entire curse area and negative curse |
| Celestial Infusion Gem | Creates an Infusion Affix regardless of progress; chooses one affix and rolls its value three times, keeping the best |
| Celestial Penance Stone | Replaces the top displayed affix among those tied for the lowest Tier; the new affix has a `5%` chance to attempt an eligible regular T0 |
| Celestial Edict Stone | Rerolls only the regular affix with the lowest relative roll within its Tier; preserves all other regular and Legendary Affixes |
| Celestial Ascension Stone | Turns Legendary equipment Mythic and raises its preserved Legendary Affix to fixed maximum-value T0 |

## Dismantling Equipment

Place at least two Runeforged items with regular affixes in a 2×2 or 3×3 crafting grid. The result is a number of Rune Fragments equal to the total regular-affix count of all inputs. Cursed, Alien, Infusion, and other special effects add no fragments. Legendary weapons cannot be dismantled.

## Rune Fragment Recipes

| Recipe | Output |
| --- | --- |
| 4 Rune Fragments + 1 Copper Ingot | 3 Shaping Stones |
| 4 Rune Fragments + 1 Iron Ingot | 3 Reinforcement Stones |
| 4 Rune Fragments + 1 Gold Ingot | 3 Reforging Stones |
| 8 Rune Fragments + 1 Redstone | 2 Stripping Stones |
| 8 Rune Fragments + 1 Lapis Lazuli | 2 Tempering Stones |

## Celestial Recipes

| Input | Output |
| --- | --- |
| 1 Ascension Stone | 4 Celestial Fragments |
| 4 Celestial Fragments | 1 Ascension Stone |
| 1 Celestial Fragment + 1 Amethyst Shard | 2 Penance Stones |
| 1 Celestial Fragment + 1 Cobblestone, Blackstone, or Cobbled Deepslate | 2 Edict Stones |
| 1 Celestial Fragment + 1 Tempering Stone | 1 Celestial Tempering Stone |
| 1 Celestial Fragment + 1 Stripping Stone | 1 Celestial Stripping Stone |
| 1 Celestial Fragment + 1 Penance Stone | 1 Celestial Penance Stone |
| 1 Celestial Fragment + 1 Edict Stone | 1 Celestial Edict Stone |
| 1 Celestial Fragment + 1 Alien Gem | 1 Celestial Alien Gem |
| 1 Celestial Fragment + 1 Sealed Gem | 1 Celestial Sealed Gem |
| 1 Celestial Fragment + 1 Infusion Gem | 1 Celestial Infusion Gem |
| 4 Ascension Stones | 1 Celestial Ascension Stone |

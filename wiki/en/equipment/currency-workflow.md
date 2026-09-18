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

Four [Infused Gems](infused-gems.md) are also craftable. Each uses one ordinary Infusion Gem in the center and eight matching materials in the outer ring.

## Quality and Regular-Affix Count

| Quality | Regular affixes |
| --- | ---: |
| Common | 0 |
| Magic | 1–3 |
| Rare | 4–5 |
| Legendary | 5, plus a Legendary Affix |

These are the normal limits. Infused Obsidian raises the Rare-or-higher regular-affix capacity to six; the other three Infused Gems lower it to four. Magic remains capped at three.

## Shaping Stone

Turns Common equipment with no regular affixes into Magic equipment and adds one random regular affix.

**Celestial version:** a Celestial Shaping Stone does not perform ordinary shaping. It selects Masterwork affixes; with two already selected, it selects a different affix to masterwork. See [Masterwork](masterwork.md).

## Reinforcement Stone

Adds one random regular affix to Magic equipment with 1–2 regular affixes, up to three. Quality remains Magic.

**Celestial version:** a Celestial Reinforcement Stone does not add a regular affix. It establishes or raises Masterwork Quality; see [Masterwork](masterwork.md).

## Tempering Stone

Adds one random regular affix to non-Cursed equipment below its regular-affix limit. At four affixes the item becomes Rare; the limit is five.

When a weapon first becomes Rare and still has no direct damage affix, the newly added affix is selected from weapon damage affixes.

**Celestial version:** a Celestial Tempering Stone adds at least T1 and has a `10%` chance to attempt an eligible regular T0, falling back to T1 when none is available.

## Reforging Stone

Clears Runeforged forging and repairs durability according to the number of removed regular affixes.

It cannot be used on Legendary equipment, any Cursed equipment (including Alien and Rune-Cursed), equipment carrying a Sealed Affix, or an item with no Runeforged equipment data. It clears quality, all mutable equipment affixes, and enchantments.

| Removed regular affixes | Maximum durability repaired |
| ---: | ---: |
| 1 | 15% |
| 2 | 30% |
| 3 | 45% |
| 4 | 75% |
| 5 or more | 100% |

At a Smithing Table, a Reforging Stone also has a separate use: combine it with target equipment and a higher-material blank weapon of the same family or armor of the same slot for [Equipment Material Upgrade](material-upgrade.md). Material Upgrade does not perform the clearing or repair operation described above.

Both ordinary and Celestial Reforging remove an [Infused Gem](infused-gems.md). A gem-modified Common item with no Runeforged equipment data can still be reforged to remove the gem.

**Celestial version:** a Celestial Reforging Stone first follows the ordinary clearing, repair, and eligibility rules, then retains one regular main affix from the item's highest Tier. Ties are resolved randomly. The retained affix keeps its name, Tier, and rolled value, and the result is Magic equipment with that single regular affix. If no regular affix can be retained, the result is the same as ordinary Reforging.

## Stripping Stone

Removes one random regular affix. The item drops from Rare to Magic below four regular affixes. Removing its final regular affix clears mutable Runeforged properties, while Sealed Affixes remain.

**Celestial version:** a Celestial Stripping Stone removes the bottom regular affix in the displayed tooltip list instead of choosing randomly.

## Penance Stone

Replaces one lowest-Tier regular affix. If several share the lowest Tier, one is selected randomly. The replacement is compatible with the item, and total affix count remains unchanged.

**Celestial version:** a Celestial Penance Stone replaces the top displayed affix among those tied for the lowest Tier. The new affix has a `5%` chance to attempt an eligible regular T0.

## Edict Stone

Rerolls the values of all non-masterworked regular affixes within their existing Tiers. Names, Tiers, count, quality, masterworked affixes, Legendary Affixes, and other special affixes remain unchanged. It cannot be used when every otherwise eligible affix is masterworked.

**Celestial version:** a Celestial Edict Stone rerolls only the non-masterworked regular affix with the lowest relative value inside its Tier. Every other affix remains unchanged.

## Ascension Stone

Turns Common, Magic, or Rare equipment Legendary, fills it to five regular affixes, and adds one T1 Legendary Affix. A Legendary weapon gains the fixed `10%` All Damage affix; Legendary armor gains fixed `10%` All Damage Reduction.

**Celestial version:** a Celestial Ascension Stone is used only on Legendary equipment. It turns the item Mythic and raises its preserved Legendary Affix to fixed maximum-value T0.

## Celestial Fragment

Rerolls the Legendary Affix on Legendary or Mythic equipment that already has one. A Mythic result remains maximum-value T0. Regular affixes, quality, the fixed Legendary bonus, Sealed Affixes, and other special effects remain unchanged.

## Sealed Gem

Turns Rare equipment into Cursed equipment.

**Eligible equipment:** Rare equipment with at least one regular affix.

Results:

- a Rare item becomes Cursed and preserves its regular affixes;
- the curse area gains 2–3 T3–T1 affixes: `75%` for two, `25%` for three;
- one negative curse is added.

**Celestial version:** a Celestial Sealed Gem can empower Rare equipment or reshape Cursed equipment. The result has exactly three curse-area affixes, including at least one T1, plus a newly rolled negative curse. When reshaping, it preserves the main-area affixes and rebuilds the entire curse area.

Sealed Gems are also ingredients for Origin Transmutation and Ancient Rune-Cursed Weapons.

## Infusion Gem

Eligible non-Common equipment gains `25–100` Infusion Value while incomplete. At `100%`, an existing Infusion Affix can be replaced and progress is cleared. Cursed equipment cannot reroll after receiving its first Infusion Affix; Nature Rune-Cursed Weapons can repeat the cycle. See [Infusion](infusion.md).

**Celestial version:** a Celestial Infusion Gem creates an Infusion Affix regardless of progress, then rolls one chosen affix's value three times and keeps the best. The target must still allow infusion; see [Infusion](infusion.md).

Infusion Gems are also ingredients for Triad Transmutation and Nature Rune-Cursed Weapons.

## Alien Gem

Turns equipment into Alien equipment and makes `1–5` random changes. A change may preserve the current affix state, replace or distort an affix, or add affixes; each Add Regular Affixes result attempts to add a random `1–5` compatible affixes. See [Alien Gem](alien-orb.md) for the full change pool, capacity, and T0 affixes.

**Celestial version:** a Celestial Alien Gem uses the same change pool and affix-capacity rules, then performs `4–6` random-change rolls; see [Celestial Alien Gem](alien-orb.md#celestial-alien-gem).

## Non-Crafted Currency Version Chances

When monsters, chests, fishing, or another non-crafted source creates a currency, it first checks for a Celestial currency. Shaping Stones, Reinforcement Stones, and Tempering Stones that do not become Celestial can then become Advanced or Sealed currency. Each item in a multi-item reward checks separately.

| Base currency | Celestial currency | If it does not become Celestial |
| --- | ---: | --- |
| Shaping Stone | `0.25%` | Monster, chest, and Elite rewards: `5%` to become an Advanced Shaping Stone or Sealed Shaping Stone; fishing: `50%`. Both outcomes are equally likely |
| Reinforcement Stone | `0.25%` | Monster, chest, and Elite rewards: `5%` to become an Advanced Reinforcement Stone or Sealed Reinforcement Stone; fishing: `50%`. Both outcomes are equally likely |
| Tempering Stone | `0.5%` | Monster, chest, and Elite rewards: `5%` to become an Advanced Tempering Stone or Sealed Tempering Stone; fishing: `50%`. Both outcomes are equally likely |
| Stripping Stone | `0.5%` | — |
| Reforging Stone, Alien Gem, Sealed Gem, Infusion Gem, Penance Stone, Edict Stone, Ascension Stone | `1%` | — |
| Celestial Fragment | — | — |

Advanced Shaping Stones, Advanced Reinforcement Stones, and Advanced Tempering Stones work like their regular counterparts and add their corresponding affix. Sealed Shaping Stones, Sealed Reinforcement Stones, and Sealed Tempering Stones also lock that affix's Tier.

Four Shaping Stones craft one Advanced Shaping Stone. Reinforcement Stones and Tempering Stones work the same way, crafting an Advanced Reinforcement Stone or Advanced Tempering Stone.

## Celestial Currency Overview

Four Ascension Stones craft one Celestial Ascension Stone directly. Other Celestial currencies use the corresponding base currency and a Celestial Fragment.

| Currency | Difference from the base version |
| --- | --- |
| Celestial Shaping Stone | Randomly masterworks up to two existing regular main affixes; with two already selected, selects a different affix to masterwork |
| Celestial Reinforcement Stone | Adds `1.0–4.0` Masterwork Quality up to the normal `25.0` cap; randomly masterworks one affix if none is selected |
| Celestial Tempering Stone | Adds at least T1; has a `10%` chance to attempt an eligible regular T0 and falls back to T1 when none is available |
| Celestial Reforging Stone | Retains one randomly selected regular main affix from the highest Tier, preserving its name, Tier, and value; the result is single-affix Magic equipment |
| Celestial Stripping Stone | Removes the bottom regular affix in the displayed list |
| Celestial Alien Gem | Uses the full Alienation change pool for `4–6` random-change rolls |
| Celestial Sealed Gem | Gives Rare equipment three curse-area affixes with at least one T1; reshapes the entire curse area and negative curse on Cursed equipment |
| Celestial Infusion Gem | Creates an Infusion Affix regardless of progress; chooses one affix and rolls its value three times, keeping the best |
| Celestial Penance Stone | Replaces the top displayed affix among those tied for the lowest Tier; the new affix has a `5%` chance to attempt an eligible regular T0 |
| Celestial Edict Stone | Among non-masterworked regular affixes, rerolls only the one with the lowest relative roll within its Tier; preserves masterworked affixes and every other regular or Legendary Affix |
| Celestial Ascension Stone | Turns Legendary equipment Mythic and raises its preserved Legendary Affix to fixed maximum-value T0 |

See [Masterwork](masterwork.md) for the complete Celestial Shaping, Celestial Reinforcement, and Masterwork Quality rules.

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
| 1 Celestial Fragment + 1 Shaping Stone | 1 Celestial Shaping Stone |
| 1 Celestial Fragment + 1 Reinforcement Stone | 1 Celestial Reinforcement Stone |
| 1 Celestial Fragment + 1 Tempering Stone | 1 Celestial Tempering Stone |
| 1 Celestial Fragment + 1 Reforging Stone | 1 Celestial Reforging Stone |
| 1 Celestial Fragment + 1 Stripping Stone | 1 Celestial Stripping Stone |
| 1 Celestial Fragment + 1 Penance Stone | 1 Celestial Penance Stone |
| 1 Celestial Fragment + 1 Edict Stone | 1 Celestial Edict Stone |
| 1 Celestial Fragment + 1 Alien Gem | 1 Celestial Alien Gem |
| 1 Celestial Fragment + 1 Sealed Gem | 1 Celestial Sealed Gem |
| 1 Celestial Fragment + 1 Infusion Gem | 1 Celestial Infusion Gem |
| 4 Ascension Stones | 1 Celestial Ascension Stone |

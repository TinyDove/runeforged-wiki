# Alien Gem

An Alien Gem turns equipment into Alien equipment and applies several random changes. The result can be dramatically stronger, weaker, or keep its current affix state.

## Using an Alien Gem

Combine one Alien Gem with any of the following in a crafting grid:

- affixable equipment that has not yet been Alienated, including Cursed and Rune-Cursed equipment;
- a Bloodthirst Rune-Cursed Weapon with remaining Alienations.

## Guaranteed Changes

- Quality becomes Cursed and the name gains the Alien prefix.
- Durability is fully restored.
- A Bloodthirst weapon consumes one remaining Alienation.

## Random Changes

A standard Alienation makes `1–5` random-change rolls. Each roll chooses equally among the changes currently included in the pool. The pool includes a blank change that preserves the current affix state, while every other change resolves from the item's current state.

| Change | Result |
| --- | --- |
| Blank change | Preserves the current affix state |
| Replace affix | Removes one random regular affix and rolls a compatible replacement |
| Add negative curse | Adds one compatible negative curse if the original item had none; removes it if the original item already had one |
| Add regular affixes | Attempts to add a random `1–5` compatible affixes, limited by remaining capacity and the available affix pool |
| Change Tier | Changes one regular affix to a different non-T0 Tier |
| Reroll value | Rerolls one regular affix inside its existing Tier |
| Add T0 | Adds one eligible Alien T0 if the item has no Alien T0 |
| Add maximum T2 | Adds one extra compatible Sealed Affix at maximum-value T2; at most once per Alienation |
| Distort highest Tier | Multiplies one highest-Tier regular affix by `0.8–1.5` |
| Empower Infusion | Multiplies an existing Infusion Affix by `1.2–1.5` |
| Break the Masterwork limit | With effective Masterwork, raises Masterwork Quality beyond its normal limit; at most once per Alienation |

Distortion can reduce the selected affix to `80%` of its former value. If the distorted regular affix crosses beyond the T1 maximum into T0, its value is normalized to that affix's fixed regular-T0 value.

Masterworked affixes are excluded from Change Tier, Reroll Value, and Distort Highest Tier. If Replace Affix selects a masterworked affix, its Masterwork selection transfers to the replacement.

Breaking the Masterwork limit can produce at most `50.0` quality. Its minimum depends on the quality before Alienation:

```text
Minimum quality = 30 + (clamp(old quality, 5, 25) - 5) × 0.5
```

An old quality of 5 or lower therefore produces `30–50`; an old quality of 25 produces `40–50`.

## Affix Count

When Add Regular Affixes is selected, it attempts to add a random `1–5` compatible affixes. The final number depends on remaining space and the available affix pool. Regular and curse-area affixes can total up to `8`, or up to `7` when the item retains a separate Legendary Affix.

## Weapon T0 Affixes

| Affix | Effect | Requirement |
| --- | --- | --- |
| Unbreakable | No durability loss | None |
| All Damage | +25% All Damage | None |
| Lightning on Hit | Additional lightning strike on hit | Existing Lightning affix |
| Explosion on Hit | Fire explosion on hit | Existing Fire affix |
| Ignore Armor | Physical attacks use an ignore-armor calculation | None |
| Keep on Death | The item is retained on player death | None |

## Armor T0 Affixes

| Affix | Effect |
| --- | --- |
| Unbreakable | No durability loss |
| All Damage Reduction | 20% less incoming damage |
| Regeneration per 5s | Restores 1 health every 5 seconds |
| Keep on Death | The item is retained on player death |

Negative-curse ranges are listed under [Cursed Equipment](curses.md).

## Celestial Alien Gem

A Celestial Alien Gem uses the same change pool and affix-capacity rules, then makes `4–6` random-change rolls.

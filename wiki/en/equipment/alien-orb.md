# Alien Gem

An Alien Gem turns equipment into Alien-Cursed equipment, fills eligible regular-affix slots, and applies several random changes.

## Use and Eligibility

Combine one affixable item and one Alien Gem in a crafting grid. Non-Cursed equipment and Rune-Cursed Weapons are eligible. Normal Cursed equipment cannot be alienated again. Alien-Cursed equipment cannot repeat the process, except a Bloodthirst Rune-Cursed Weapon with remaining Alienations.

## Guaranteed Changes

- Quality becomes Cursed and the name gains the Alien prefix.
- Durability is fully restored.
- Existing regular, Rune fixed, Sealed, and T0 affixes remain.
- The existing negative curse is removed; the Alien changes may add another.
- A Bloodthirst weapon consumes one remaining Alienation.

## Regular-Affix Fill

When used on Common, Magic, or Rare equipment, the gem first fills regular affixes: `0–2` existing affixes become `3`; `3–4` become `5`; equipment with `5` or more gains one, up to its limit. Legendary equipment and Rune-Cursed Weapons eligible for another Alienation skip this step.

## Random Changes

A standard Alienation then makes `1–5` rolls. Each roll chooses equally among changes that the item can receive:

| Change | Result |
| --- | --- |
| Replace affix | Removes one random regular affix and rolls a compatible replacement |
| Add negative curse | Adds one compatible negative curse if none exists |
| Add regular affix | Adds one compatible regular affix if below the limit |
| Change Tier | Changes one regular affix to a different non-T0 Tier |
| Reroll value | Rerolls one regular affix inside its existing Tier |
| Add T0 | Adds one eligible Alien T0 if the item has none |
| Add maximum T2 | Adds one extra compatible Sealed Affix at maximum-value T2; at most once per Alienation |
| Distort highest Tier | Multiplies one highest-Tier regular affix by `0.8–1.5` |
| Empower Infusion | Multiplies an existing Infusion Affix by `1.2–1.5` |

Distortion can reduce the selected affix to `80%` of its former value.

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

A Celestial Alien Gem uses the same regular-affix fill and then makes `4–6` random-change rolls.

## Generated Alien Equipment

Some Cursed equipment from monsters, chests, or fishing has a `10%` chance to become Alien immediately and receive `1–5` random changes.

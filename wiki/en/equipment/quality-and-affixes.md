# Equipment Quality & Affixes

## Equipment Quality

| Quality | Color | Base regular affixes | Regular currency use |
| --- | --- | ---: | --- |
| Common | White | 0 | Yes |
| Magic | Blue | 1–3 | Yes |
| Rare | Pink | 4–5 | Yes |
| Legendary | Orange | 5, plus a Legendary Affix | Yes, with restrictions on some currencies |
| Mythic | Red | 5, plus a maximum-value T0 Legendary Affix | Only explicitly supported special currencies |
| Cursed | Purple | Depends on source | Usually no |

Quality affects the chance of rolling a higher affix Tier, but does not guarantee the highest Tier.

The table shows capacity without an [Infused Gem](infused-gems.md). At Rare quality or higher, Infused Obsidian raises regular-affix capacity to `6`, while Infused Amethyst, Lapis Lazuli, and Ruby reduce it to `4`. Common remains at `0` and Magic remains capped at `3`. These changes apply only to regular main affixes, not special-affix layers.

## Affix Tiers

Regular affixes are ordered from T4 to T1. Some affixes do not have all four Tiers. Affixes with the same name and Tier may also roll different values; rerolling values does not change their name or Tier.

### Regular T0 Affixes

A regular affix that supports T1 can rarely break through to T0. It keeps the original affix name, eligible equipment, and conflict rules, occupies one regular-affix slot, and has a fixed value equal to `120%` of that affix's maximum T1 value.

Regular T0 can appear on equipment from non-crafted sources such as monsters, chests, or fishing. It can also result when Alien distortion pushes a regular affix beyond the T1 maximum. Celestial Tempering Stones and Celestial Penance Stones can produce regular T0 as well.

- [Weapon Affixes](../reference/weapon-affixes.md)
- [Armor Affixes](../reference/armor-affixes.md)

## Masterworked Affixes

Masterwork is not another affix type and does not occupy an additional affix slot. It selects up to `2` regular main affixes and raises their effective values according to the item's Masterwork Quality. A selected affix displays `Tier+`, such as `T1+`.

See [Masterwork](masterwork.md) for the multiplier, Celestial Shaping and Reinforcement Stones, and currency interactions.

## Special Affixes

| Type | Main source | Details |
| --- | --- | --- |
| Legendary Affix | Ascension Stone or generated Legendary equipment | [Equipment Currency](currency-workflow.md) |
| Sealed Affix | Sealed Gem | [Equipment Currency](currency-workflow.md) |
| Infusion Affix | Combat infusion or Infusion Gem | [Infusion](infusion.md) |
| Infused Gem modifier | Infused Obsidian, Amethyst, Lapis Lazuli, or Ruby | [Infused Gems](infused-gems.md) |
| Curse-area and negative affixes | Generated Cursed equipment or Sealed Gem | [Cursed Equipment](curses.md) |
| Alien T0 and distorted affixes | Alien Gem | [Alien Gem](alien-orb.md) |
| Rune fixed affixes | Rune-Cursed Weapons | [Rune-Cursed Weapons](rune-cursed-weapons.md) |

Regular-affix operations do not affect these special affixes unless the relevant currency explicitly says otherwise.

## Affix Conflicts

Some affixes cannot coexist. The three Slayer affixes conflict with one another, as do the four physical conversions and the four Blessings. Fire conflicts with certain Frost affixes, Lightning with certain Holy affixes, and armor reduction or Shelter affixes have their own conflict groups. Complete rules are listed in the weapon and armor affix tables.

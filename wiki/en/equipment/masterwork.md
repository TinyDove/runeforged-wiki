# Masterwork

Masterwork selects regular main affixes on an item and raises their effective values according to the item's Masterwork Quality. It does not add affixes or change their Tiers.

## Effect and Display

For Masterwork Quality `Q`, a masterworked affix uses:

```text
Effective value = original affix value × (1 + Q / 100)
```

At `20.0` Masterwork Quality, for example, each masterworked affix is `20%` stronger. One item can have at most `2` masterworked affixes.

- A masterworked affix displays `Tier+`, such as `T1+`.
- The tooltip displays Masterwork Quality to one decimal place.
- All resolved regular weapon and armor affixes use the same multiplier, including damage, mitigation, Health, and Durability.
- Legendary, Infusion, Sealed, fixed Rune, and Curse Affixes cannot be masterworked.

## Eligible Equipment

Celestial Shaping Stones and Celestial Reinforcement Stones work on non-Cursed equipment with at least one regular main affix, including Magic, Rare, Legendary, and Mythic equipment.

They cannot be applied directly to Cursed equipment. A masterworked item may be Alienated afterward; Alienation preserves Masterwork and can push its quality beyond the normal limit.

## Celestial Shaping Stone

The Celestial Shaping Stone selects masterworked affixes:

- With none selected, it randomly selects up to `2` existing regular main affixes.
- With `1` selected, it randomly selects `1` other regular main affix.
- With `2` selected and other main affixes available, it deselects `1` at random and selects `1` unselected affix.
- It cannot be used when every regular main affix on the item is already selected.

Creating the first masterworked affix sets Masterwork Quality to `1.0`.

## Celestial Reinforcement Stone

The Celestial Reinforcement Stone raises Masterwork Quality:

- Each use adds `1.0–4.0` in steps of `0.1`.
- Normal Masterwork Quality is capped at `25.0`.
- It cannot be used at `25.0`.
- If the item has no masterworked affix, it first selects `1` regular main affix at random.

If the item has no stored Masterwork Quality, its first direct Celestial Reinforcement use also establishes the initial `1.0` quality, so the resulting total is `2.0–5.0`. If the item retains stored quality but has no masterworked affix, the stone selects one affix and adds only the usual `1.0–4.0`, up to the `25.0` cap.

## Currency Interactions

- **Edict Stone and Celestial Edict Stone:** do not reroll masterworked affixes; they affect only non-masterworked affixes.
- **Stripping Stone and Celestial Stripping Stone:** can remove a masterworked affix. Its Masterwork selection is then removed.
- **Penance Stone and Celestial Penance Stone:** replacing a masterworked affix with a different affix removes its selection; it does not transfer automatically. A replacement with the same affix name can retain the selection.
- **Reforging Stone:** clears regular affixes and Masterwork selections, but preserves the Masterwork Quality already accumulated on the item.
- **Celestial Shaping Stone:** can later use that preserved quality when selecting affixes again.

Masterwork Quality belongs to the item itself. It does not reset when every masterworked affix is removed; while no affix is selected, the stored quality provides no stat bonus.

## Alienation

Alienation protects Masterwork state:

- Tier changes, within-Tier value rerolls, and highest-Tier distortion skip masterworked affixes.
- If affix replacement selects a masterworked affix, its Masterwork selection transfers to the replacement.
- Equipment with effective Masterwork can roll the Masterwork overlimit change described in [Alien Gem](alien-orb.md).

## Obtaining the Currency

Each currency can be crafted from its base currency and a Celestial Fragment. A single non-crafted Shaping Stone or Reinforcement Stone also has a `0.25%` chance to become its Celestial version.

See [Equipment Currency](currency-workflow.md) for complete recipes and the other Celestial currencies.

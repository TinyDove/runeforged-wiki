# Cursed Equipment

Cursed is a separate equipment quality. Generated Normal and Sealed Cursed equipment generally contains regular affixes, curse-area affixes, and one negative curse; Alien and Rune-Cursed equipment use their own structures.

## Core Rules

- Cursed equipment cannot use ordinary forging currency to add or remove affixes.
- It cannot be enchanted or repaired.
- It can hold up to `8` regular and curse-area affixes. Negative curses, Sealed Affixes, Infusion Affixes, and Alien T0 affixes are displayed separately.
- Special gems still work where their own rules allow them.

## Generated Cursed Equipment

Generated monster weapons have a default `20%` chance to become Cursed. Chests, fishing, and merchants can also produce Cursed equipment.

A generated Cursed item normally has:

- `3–4` base regular affixes;
- `2–3` curse-area affixes: `75%` for two, `25%` for three;
- curse-area Tiers from T4 through T1;
- one compatible negative curse;
- `0–75%` initial Infusion Value;
- a `10%` chance to immediately undergo 1–5 Alien changes.

## Cursed Variants

| Variant | Main source | Structure and follow-up rules |
| --- | --- | --- |
| Normal Cursed | Monsters, chests, fishing, trades | Regular affixes, 2–3 curse-area affixes, one negative curse; eligible for Sealed Gem reroll or generated Alienation |
| Sealed Cursed | Sealed Gem on eligible Rare or Cursed equipment | Preserves regular affixes; curse area uses T3–T1; another Sealed Gem rerolls the entire curse area and negative curse |
| Alien-Cursed | Alien Gem or generated Alienation | 1–5 random changes, possibly T0, an extra maximum-value T2 Sealed Affix, or distortion; see [Alien Gem](alien-orb.md) |
| Rune-Cursed | Blank weapon plus specified currency | Fixed archetype affixes and additional random affixes; see [Rune-Cursed Weapons](rune-cursed-weapons.md) |

## Weapon Negative Curses

| Negative curse | Range | Eligible equipment |
| --- | ---: | --- |
| Max Durability | `-75%–0%` | All equipment |
| Attack Range | `-1–0` | Eligible melee weapons |
| Attack Speed | `-25%–0%` | Eligible melee weapons |
| Knockback Distance | `-100%–0%` | Eligible melee weapons |
| Physical Damage | `-50%–0%` | Weapons |
| Elemental Damage | `-75%–0%` | Weapons |
| Projectile Speed | `-50%–0%` | Ranged weapons |
| Bow Draw Speed | `-25%–0%` | Bows |
| Crossbow Charge Speed | `-25%–0%` | Crossbows |

## Armor and General Negative Curses

| Negative curse | Range | Effect |
| --- | ---: | --- |
| Max Health | `-4–0` | Reduces maximum health |
| Armor | `-20%–0%` | Percentage reduction to total Armor |
| Armor Toughness | `-50%–0%` | Percentage reduction to total Armor Toughness |
| Movement Speed | `-12%–0%` | Reduces Movement Speed |
| Elemental Damage Taken | `0%–+40%` | Increases incoming elemental damage |
| Debuff Duration | `0%–+40%` | Extends negative status effects |
| Gluttony | `0–0.5` each time | Consumes food when the weapon hits or the armor wearer takes damage; fractional values trigger probabilistically |
| Natural Regeneration | `-50%–0%` | Reduces natural healing, including Peaceful food and saturation recovery |

Only compatible negative curses can appear. A bow cannot receive melee Attack Range, and armor cannot receive weapon damage penalties.

## Infusion

Normal, Sealed, and Alien-Cursed equipment can gain its first Infusion Affix but cannot reroll afterward. Nature Rune-Cursed Weapons use the complete repeatable cycle. See [Infusion](infusion.md).

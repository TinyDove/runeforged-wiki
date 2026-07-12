# Default Configuration

Probabilities and scaling in this wiki use a fresh installation's defaults. A server may save custom configuration, so its settings take precedence.

## `runeforged-general.json`

### Display

| Setting | Default |
| --- | --- |
| `welcome_message_mode` (welcome message) | `first_join_once` |
| `damage_popups_enabled` (damage popups) | Enabled |
| `normal_monster_nameplates_enabled` (normal monster nameplates) | Enabled |
| `elite_monster_nameplates_enabled` (Elite monster nameplates) | Enabled |
| `elite_boss_bars_enabled` (Elite boss bars) | Enabled |

### Monster Progression and Elites

| Setting | Default |
| --- | ---: |
| Monster levels | Enabled |
| World progression | Enabled |
| Maximum random bonus level | 5 |
| Random bonus level stage factor | 2.0 |
| Elite system | Enabled |
| Base Elite chance | 1.0% |
| Elite chance per level | +0.02 percentage points |
| Minimum Elite Affixes | 1 |
| Random Elite chunk cap | Disabled |
| Random Elite base chunk cap when enabled | 1 |
| Extra persistent Elite allowance when enabled | 1 |
| Elite chance level cap | 100 |
| Maximum Elite Affixes | 4 |

### Loot and Combat

| Setting | Default |
| --- | ---: |
| Monster currency drops | Enabled, ×1.0 |
| Extra Elite drops | Enabled, chance and quantity ×1.0 |
| Fishing replacement pool | Enabled, ×1.0 |
| Chest rewards | Enabled, chance and quantity ×1.0 |
| Weapon Skills | Enabled |
| Infusion | Enabled |
| Weakness damage hint threshold | Resistance ≤ -20% |

### Monster Damage Soft Cap

Enabled by default. Marginal damage is retained according to cumulative damage:

| Cumulative damage | Marginal multiplier |
| --- | ---: |
| 0–12 | 100% |
| 12–18 | 60% |
| 18–24 | 40% |
| 24–32 | 30% |
| 32+ | 20% |

Additional defaults include a `25` threshold and a `+0.5%` threshold adjustment per monster level.

## Other Configuration Files

- `runeforged-affixes.json`: affix ranges, value types, and configuration version.
- `runeforged-monsters.json`: area levels, stat scaling, currency chance, equipment quality, chest tiers, and reward pools.
- `runeforged-compat.json`: compatibility migrations and external-content adaptations.

See [Weapon Affixes](weapon-affixes.md), [Armor Affixes](armor-affixes.md), and [Monster Drops](../obtaining/monster-drops.md) for the complete player-facing defaults.

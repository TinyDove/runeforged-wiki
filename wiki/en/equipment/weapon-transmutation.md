# Weapon Transmutation

Runeforged has seven Transmutations: Heavy, Sharp, Pure, Order, Mystery, Origin, and Triad. They are applied at a Smithing Table with a Reforging Stone. A Transmutation is a fixed affix, does not consume a regular-affix slot, and a weapon can have only one at a time. Applying another directly replaces it.

## Smithing Table Recipes

| Template slot | Base slot | Addition slot | Result |
| --- | --- | --- | --- |
| Shaping Stone | Weapon | Reforging Stone | Heavy |
| Reinforcement Stone | Weapon | Reforging Stone | Sharp |
| Stripping Stone | Weapon | Reforging Stone | Pure |
| Tempering Stone | Weapon | Reforging Stone | Order |
| Alien Gem | Weapon | Reforging Stone | Mystery |
| Sealed Gem | Weapon | Reforging Stone | Origin |
| Infusion Gem | Weapon | Reforging Stone | Triad |

The base must be one affixable, non-Cursed weapon. Applying the same Transmutation produces no result; another Transmutation is replaced directly.

To remove a Transmutation, place a Reforging Stone in both the template and addition slots and the transmuted weapon in the base slot. Its quality and regular affixes are unaffected.

## Effects

| Transmutation | Selection item | Fixed effect |
| --- | --- | --- |
| Heavy | Shaping Stone | `+25%` Physical Damage; `-50%` Elemental Damage; `-10%` Attack Speed |
| Sharp | Reinforcement Stone | `-40%` base Physical Damage; `+50%` Physical Damage |
| Pure | Stripping Stone | `50%` Physical converted to Holy; `-25%` Physical Damage; `-75%` Fire/Frost/Lightning Damage |
| Order | Tempering Stone | When several damage types are present: highest type `-25%`, lowest type `+50%` |
| Mystery | Alien Gem | `+20%` Critical Strike Chance; non-critical hits `-20%` Elemental Damage; critical hits `-20%` Physical Damage |
| Origin | Sealed Gem | Highest element `+15%`; all other damage `-30%` |
| Triad | Infusion Gem | `-50%` Physical Damage; rotating Fire–Frost / Frost–Lightning / Lightning–Fire pair gains `+25%` |

## Order and Triad

Order records the highest and lowest damage buckets of a multi-type hit. On the next calculation, the recorded highest receives `-25%` and the lowest `+50%`. Replacing or removing the Transmutation clears the record.

Triad advances its empowered pair after every hit: Fire–Frost → Frost–Lightning → Lightning–Fire → Fire–Frost. Physical Damage always receives `-50%`; replacing or removing the Transmutation resets the cycle.

## Generated Transmutations

Eligible generated weapons have a `5%` chance to carry a Transmutation. A weapon with one cannot roll another, and Rune-Cursed Weapons do not receive generated Transmutations. Sources include monster weapons, chest weapon rewards, and some treasure-generated weapons.

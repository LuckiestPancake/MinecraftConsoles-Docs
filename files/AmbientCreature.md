# AmbientCreature

## Purpose
The base class for ambient mobs that do not interact much with the player or environment, such as bats.

## Key Classes
- **AmbientCreature**: Inherits from both `Mob` and `Creature`.

## Important Functions
- `canBeLeashed()`: Always returns false for ambient creatures.
- `mobInteract()`: Always returns false.

## Modding Notes
Used as a lightweight base for mobs that are mostly for atmosphere.

## Important Dependencies
- `Mob.h`
- `Creature.h`

[Category: Entities]

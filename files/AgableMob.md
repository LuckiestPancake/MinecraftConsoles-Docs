# AgableMob

## Purpose
The base class for all mobs that have a growth lifecycle (baby to adult). It manages age, growth timers, and size scaling.

## Key Classes
- **AgableMob**: Inherits from `PathfinderMob`.

## Important Functions
- `ageUp()`: Increases the age of the mob.
- `setAge()`: Sets the mob's age (negative for babies, positive/zero for adults).
- `isBaby()`: Returns true if the mob is currently a baby.
- `updateSize()`: Adjusts the bounding box based on whether the mob is a baby.
- `mobInteract()`: Handles interactions, such as using a spawn egg to create a baby version of the mob.

## Modding Notes
Uses `SynchedEntityData` (DATA_AGE_ID) to synchronize age across the network. Scale for babies is hardcoded to 0.5f in `updateSize`.

## Important Dependencies
- `PathfinderMob.h`
- `SynchedEntityData.h`

[Category: Entities]

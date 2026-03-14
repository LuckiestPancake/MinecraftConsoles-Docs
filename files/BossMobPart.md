# BossMobPart.h / BossMobPart.cpp

## Purpose
Represents a sub-section of a larger boss entity (e.g., the segments of the Ender Dragon's body or wings). This allows for complex collision and damage systems on large mobs.

## Key Classes
- `BossMobPart`: Inherits from `Entity`.

## Important Functions
- `hurt()`: Forwards damage taken by the part to the parent `BossMob`.
- `is()`: Helper to check if an entity is either this part or the parent boss.
- `isPickable()`: Always returns true so the part can be hit.

## Modding Notes
- Each part has its own size and bounding box but no independent AI.
- Relates to **entities**.

## Important Dependencies
- `Entity.h`
- `BossMob.h`

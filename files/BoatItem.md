# BoatItem.h / BoatItem.cpp

## Purpose
The item used to place a Boat entity into the world.

## Key Classes
- `BoatItem`: Inherits from `Item`.

## Important Functions
- `use()`: Triggered when a player right-clicks while holding a boat. It performs a raycast to find water or land, checks for entity collisions, and spawns a `Boat` entity if successful.
- `TestUse()`: 4J Studios added this to provide UI tooltips showing if a boat can be placed at the current crosshair location.

## Modding Notes
- Raycasting distance is set to 5 blocks.
- Includes a check against `Level::MAX_XBOX_BOATS` and displays a console-specific message (`IDS_MAX_BOATS`) if the limit is reached.
- Relates to **items** and **entities**.

## Important Dependencies
- `Item.h`
- `Boat.h`
- `Level.h`
- `HitResult.h`
- `Player.h`

# BedItem.h / BedItem.cpp

## Purpose
An item used to place Bed blocks in the world.

## Key Classes
- `BedItem`: Inherits from `Item`.

## Important Functions
- `useOn()`: Handles the logic for placing a bed. It checks for a 2x1 clear area on top of solid blocks and places the foot and head pieces with the correct orientation.

## Modding Notes
- Orientation is determined by the player's rotation at the time of placement.
- 4J Studios added a `bTestUseOnOnly` parameter to support placement tooltips without actually placing the block.
- Relates to **items** and **blocks**.

## Important Dependencies
- `BedTile.h`
- `Facing.h`
- `GenericStats.h`

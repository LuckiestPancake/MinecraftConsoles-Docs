# BaseEntityTile.h / BaseEntityTile.cpp

## Purpose
A base class for blocks (tiles) that are associated with a `TileEntity`. It handles the basic logic of placing and removing the associated `TileEntity` when the block is added or destroyed in the world.

## Key Classes
- `BaseEntityTile`: Inherits from `Tile` and implements the `EntityTile` interface.

## Important Functions
- `onPlace()`: Called when the block is placed; traditionally used to create the `TileEntity`.
- `onRemove()`: Called when the block is removed; ensures the `TileEntity` is also removed from the level.
- `triggerEvent()`: Passes block events (like a chest opening) to the associated `TileEntity`.

## Modding Notes
- Most interactive blocks (chests, furnaces, signs) inherit from this class.
- Relates to **entities** (TileEntities).

## Important Dependencies
- `Tile.h`
- `EntityTile.h`
- `TileEntity.h`
- `Level.h`

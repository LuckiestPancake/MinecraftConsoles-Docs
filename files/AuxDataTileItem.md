# AuxDataTileItem.h / AuxDataTileItem.cpp

## Purpose
A specialized `TileItem` that uses auxiliary (metadata) data to determine its appearance and properties. Commonly used for tiles that share an ID but have multiple variants (e.g., different types of wood or colored wool).

## Key Classes
- `AuxDataTileItem`: Inherits from `TileItem`.

## Important Functions
- `getIcon()`: Returns the icon for a specific auxiliary value by querying the parent `Tile`.
- `getLevelDataForAuxValue()`: Maps the item's auxiliary value to the block's data value in the world.

## Modding Notes
- Useful for adding new multi-variant blocks without consuming many block IDs.
- Relates to **entities** (as items are entities when dropped) and **rendering** (icons).

## Important Dependencies
- `TileItem.h`
- `net.minecraft.world.level.tile.h`

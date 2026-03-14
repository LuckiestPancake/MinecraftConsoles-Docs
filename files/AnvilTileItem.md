# AnvilTileItem

## Purpose
The item form of the Anvil block, handling its representation in inventories and how it places the block with specific metadata.

## Key Classes
- **AnvilTileItem**: Inherits from `MultiTextureTileItem`.

## Important Functions
- `getLevelDataForAuxValue()`: Converts the item's auxiliary value into block metadata.
- `getDescriptionId()`: Returns the localized name based on the anvil's damage state.

## Modding Notes
Manages the three damage variants of the anvil as a single item type with different metadata.

## Important Dependencies
- `MultiTextureTileItem.h`
- `AnvilTile.h`

[Category: Entities]

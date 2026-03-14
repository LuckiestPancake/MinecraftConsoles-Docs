# BonusChestFeature

## Purpose
Handles the generation of the "Bonus Chest" that can spawn near the player's initial spawn point in a new world.

## Key Classes
- **BonusChestFeature**: A feature class that inherits from `Feature` and handles chest placement and loot generation.

## Important Functions
- **place(Level *level, Random *random, int x, int y, int z)**: Standard feature placement method.
- **place(Level *level, Random *random, int x, int y, int z, bool force)**: 4J-added method that includes a `force` parameter to guarantee placement near the spawn point if the initial attempt fails. It also places torches around the chest.

## Modding Notes
- Only spawns if `level->isNew` is true.
- Uses `WeighedTreasure::addChestItems` to populate the chest.
- Marks the chest tile entity with `isBonusChest = true`.

## Important Dependencies
- `Feature`
- `Level`
- `ChestTileEntity`
- `WeighedTreasure`

## Category
- World Generation
- Entities

## Cross-references
- [[Feature]]
- [[ChestTileEntity]]
- [[WeighedTreasure]]

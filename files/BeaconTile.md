# BeaconTile.h / BeaconTile.cpp

## Purpose
The block class for the Beacon. It handles block properties, placement, and interaction (opening the UI).

## Key Classes
- `BeaconTile`: Inherits from `BaseEntityTile`.

## Important Functions
- `newTileEntity()`: Creates a new `BeaconTileEntity` for this block.
- `use()`: Opens the beacon's interface when a player right-clicks the block.
- `setPlacedBy()`: Passes a custom name from the item (if renamed in an anvil) to the TileEntity.

## Modding Notes
- Is a transparent/glass material block.
- Relates to **blocks** and **UI**.

## Important Dependencies
- `BaseEntityTile.h`
- `BeaconTileEntity.h`
- `Player.h`

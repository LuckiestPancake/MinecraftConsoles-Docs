# BlockSource.h / BlockSourceImpl.h / BlockSourceImpl.cpp

## Purpose
Provides an abstraction layer for interacting with a block in the world. Instead of passing coordinates and level pointers separately, a `BlockSource` object encapsulates the position and provides easy access to the block's type, data, and TileEntity.

## Key Classes
- `BlockSource`: Abstract interface.
- `BlockSourceImpl`: Concrete implementation holding a `Level*` and (x, y, z) coordinates.

## Important Functions
- `getType()`: Returns the `Tile*` at the source position.
- `getData()`: Returns the metadata value.
- `getEntity()`: Returns the `TileEntity*` if one exists at the position.
- `getX()` / `getY()` / `getZ()`: Returns the center coordinates of the block as doubles.

## Modding Notes
- This is often used by AI goals or block behaviors (like Dispensers) to query their environment cleanly.
- Relates to **world** and **AI**.

## Important Dependencies
- `LocatableSource.h`
- `Level.h`
- `Tile.h`
- `TileEntity.h`

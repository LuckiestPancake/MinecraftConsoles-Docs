# BlockReplacements.h / BlockReplacements.cpp

## Purpose
Provides a utility to validate and replace invalid block IDs in a buffer. It ensures that any ID that doesn't correspond to a registered `Tile` is replaced with air (ID 0).

## Key Classes
- `BlockReplacements`: Utility class.

## Important Functions
- `staticCtor()`: Initializes a 256-byte lookup table where invalid IDs are mapped to 0.
- `replace()`: Processes a `byteArray` of blocks, replacing invalid ones using the lookup table.

## Modding Notes
- This is a safety measure used during world loading or generation to prevent crashes from dangling block IDs.
- Relates to **world generation** and **core utility**.

## Important Dependencies
- `Tile.h`
- `ArrayWithLength.h`

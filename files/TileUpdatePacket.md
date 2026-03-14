# TileUpdatePacket

## Purpose
The `TileUpdatePacket` is used to update a single block at a specific coordinate, including its block ID and metadata.

## Key Classes
- **TileUpdatePacket**: The packet class for single block updates.
- **Level**: The world level where the block is located.

## Important Functions
- **TileUpdatePacket(int x, int y, int z, Level *level)**: Constructor that captures the current state of a block at the given position.
- **read(DataInputStream *dis)**: Reads the coordinates, block ID, and metadata. Uses aggressive bit-packing for efficiency.
- **write(DataOutputStream *dos)**: Writes the packed block data.

## Modding Notes
- The 4J implementation uses significant bit-packing to fit the X, Y, Z, and metadata into a single integer where possible.
- Support for `_LARGE_WORLDS` exists with a different, less-packed format.
- Categorized under **Rendering** and **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.world.level.h`
- `Dimension.h`

---
**Related to:** [Rendering](Rendering.md), [Networking](Networking.md)

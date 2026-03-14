# BlockRegionUpdatePacket.h / BlockRegionUpdatePacket.cpp

## Purpose
A network packet used to send a bulk update of block and data values for a specific region (often an entire chunk) to the client.

## Key Classes
- `BlockRegionUpdatePacket`: Inherits from `Packet`.

## Important Functions
- `BlockRegionUpdatePacket(x, y, z, xs, ys, zs, Level*)`: Constructor that gathers block data from the world and compresses it.
- `read()` / `write()`: Handles serialization, including complex chunk flags and compression logic.
- `handle()`: Dispatches the packet to the `PacketListener`.

## Modding Notes
- Packet ID is 51.
- 4J Studios uses `LZXRLE` compression for block data to optimize network bandwidth.
- Includes a optimization for "full chunks" (16x256x16) where blocks are reordered for better compression.
- Relates to **networking** and **world generation** (syncing chunks).

## Important Dependencies
- `Packet.h`
- `compression.h`
- `LevelChunk.h`
- `DataInputStream.h`
- `DataOutputStream.h`

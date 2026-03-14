# ChunkTilesUpdatePacket

## Purpose
Updates multiple blocks (tiles) within a single chunk in a single network transmission. This is more efficient than sending individual `TileUpdatePacket` calls when several blocks change simultaneously.

## Key Classes
- **ChunkTilesUpdatePacket**: Inherits from `Packet` to handle batch tile updates.

## Important Functions
- `read()`: Decodes chunk coordinates, block positions, and new tile data.
- `write()`: Encodes the batch update data.
- `handle()`: Dispatches the update to the `PacketListener`.
- `getId()`: Returns the packet ID (52).

## Modding Notes
4J Studios optimized the `count` field from an `int` to a `byte`, as their implementation never exceeds 10 updates per packet in this batch format. This saves bandwidth in every packet sent.

## Important Dependencies
- `Packet.h`
- `Level.h`
- `PacketListener.h`

[Category: Networking, Rendering]

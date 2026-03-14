# ChunkVisibilityPacket

## Purpose
Updates the visibility status of a single chunk for a client. It tells the client whether a specific chunk should be rendered or cleared from memory.

## Key Classes
- **ChunkVisibilityPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes the chunk coordinates (x, z) and the visibility boolean.
- `write()`: Encodes the chunk position and visibility state.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (50).

## Modding Notes
This is a standard packet for managing chunk lifecycle on the client side, ensuring that only chunks near the player are active.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking, Rendering]

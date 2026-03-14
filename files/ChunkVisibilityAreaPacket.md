# ChunkVisibilityAreaPacket

## Purpose
A 4J Studios-specific optimization packet used to notify a client of a rectangular area of chunks that should be considered visible. This is primarily used when a player initially joins the game to load the surrounding world efficiently.

## Key Classes
- **ChunkVisibilityAreaPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes the min/max X and Z coordinates defining the visibility area.
- `write()`: Encodes the rectangular bounds.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (155).

## Modding Notes
This packet replaces the need to send dozens of individual `ChunkVisibilityPacket` calls when a player spawns, significantly reducing the initial network overhead during world entry.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking, Rendering]

# DebugOptionsPacket

## Purpose
A 4J Studios-specific packet used to transmit debug flags or settings between the client and server.

## Key Classes
- **DebugOptionsPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes an unsigned integer bitfield (`m_uiVal`) of debug options.
- `write()`: Encodes the debug flags.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (152).

## Modding Notes
This packet is likely used for toggling development-time features like wireframe rendering, coordinate overlays, or other engine-level debug tools without requiring a full game restart or specialized command.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking]

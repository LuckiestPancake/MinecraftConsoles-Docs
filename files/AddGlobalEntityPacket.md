# AddGlobalEntityPacket

## Purpose
A network packet for spawning "global" entities, primarily used for lightning bolts, which need to be visible to all players regardless of distance.

## Key Classes
- **AddGlobalEntityPacket**: Inherits from `Packet` for global entity notifications.

## Important Functions
- `read()`/`write()`: Handles ID, type, and position.
- `handle()`: Dispatches to `PacketListener`.
- `getId()`: Returns the packet ID (71).

## Modding Notes
Currently primarily supports the `LIGHTNING` type.

## Important Dependencies
- `Packet.h`
- `Entity.h`

[Category: Networking]

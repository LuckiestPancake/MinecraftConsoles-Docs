# AddEntityPacket

## Purpose
A network packet sent by the server to clients to notify them of a new non-living entity (like boats, items, minecarts, projectiles) being added to the world.

## Key Classes
- **AddEntityPacket**: Inherits from `Packet` to handle entity spawning data over the network.

## Important Functions
- `read()`: Decodes packet data from a `DataInputStream`.
- `write()`: Encodes packet data to a `DataOutputStream`.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (23).

## Modding Notes
4J Studios added support for `_LARGE_WORLDS` using 32-bit integers for coordinates instead of 16-bit shorts. They also added specific entity types like `DRAGON_FIRE_BALL`.

## Important Dependencies
- `Packet.h`
- `Entity.h`
- `PacketListener.h`

[Category: Networking]

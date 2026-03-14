# ContainerOpenPacket

## Purpose
Sent by the server to the client to trigger the opening of a specific container GUI, providing the necessary metadata like type, size, and title.

## Key Classes
- **ContainerOpenPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes the container ID, type, title, size, and optional entity ID.
- `write()`: Encodes the opening parameters.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (100).

## Modding Notes
4J Studios significantly expanded the available container types beyond the standard Java set. Custom types include `FIREWORKS` (12), `BONUS_CHEST` (13), `LARGE_CHEST` (14), `ENDER_CHEST` (15), `MINECART_CHEST` (16), and `MINECART_HOPPER` (17). This packet can also carry a custom name for the container if `customName` is true.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking, UI]

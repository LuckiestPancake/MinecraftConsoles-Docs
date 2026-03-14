# ComplexItemDataPacket

## Purpose
Transmits detailed, non-standard data for complex items that cannot be represented by simple ID and metadata. A primary example is Map data, where the packet carries the actual image/pixel data for the map.

## Key Classes
- **ComplexItemDataPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes item type, item ID, and the raw byte array of data.
- `write()`: Encodes the complex item data for the client.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (131).

## Modding Notes
Uses a `charArray` (effectively a byte array) to carry the payload. This is essential for items whose state is too large for the standard `EntityData` system.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking, Entities]

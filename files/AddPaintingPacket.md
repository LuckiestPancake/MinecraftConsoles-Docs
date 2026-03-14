# AddPaintingPacket

## Purpose
A network packet used to notify clients that a painting has been placed in the world.

## Key Classes
- **AddPaintingPacket**: Inherits from `Packet` to communicate painting placement.

## Important Functions
- `read()`/`write()`: Handles entity ID, tile coordinates (x, y, z), direction, and the specific motive (art piece) of the painting.
- `handle()`: Dispatches to `PacketListener`.

## Modding Notes
Uses the `Painting::Motive` name to identify which piece of art to display.

## Important Dependencies
- `Packet.h`
- `Painting.h`

[Category: Networking]

# ContainerSetDataPacket

## Purpose
Updates a specific internal property of an open container GUI. This is used for values that change over time, such as the progress bar in a furnace (cook time) or the available enchantment levels in an Enchantment Table.

## Key Classes
- **ContainerSetDataPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes the `containerId`, the data property `id`, and the property `value`.
- `write()`: Encodes the property update.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (105).

## Modding Notes
This packet allows the client's GUI to accurately reflect server-side processing (like smelting progress) without having to sync the entire container state.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking, UI]

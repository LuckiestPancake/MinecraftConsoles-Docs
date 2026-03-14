# ContainerButtonClickPacket

## Purpose
A packet sent from the client to the server when a player interacts with a button inside a container's interface. This is commonly used for interfaces like the Enchantment Table (selecting an enchantment) or the Beacon (selecting a power).

## Key Classes
- **ContainerButtonClickPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes the `containerId` and the `buttonId`.
- `write()`: Encodes the click data.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (108).

## Modding Notes
This packet is specifically for UI-driven logic where a simple "click" isn't enough, but a specific button action within that container context is required.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking, UI]

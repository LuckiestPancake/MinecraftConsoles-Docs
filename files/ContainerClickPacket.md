# ContainerClickPacket

## Purpose
Sent by the client to the server whenever a player interacts with a slot in an open container (chest, inventory, furnace, etc.). It describes the nature of the click and the items involved.

## Key Classes
- **ContainerClickPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes container ID, slot number, button used, click type, item instance, and unique transaction ID (`uid`).
- `write()`: Encodes the complex click interaction.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (102).

## Modding Notes
This is one of the most complex packets in the inventory system. It uses a `uid` to match with a `ContainerAckPacket` from the server, ensuring that high-latency connections don't result in desynchronized inventories. It supports multiple `clickType` values to handle normal clicks, shift-clicks, and other complex interactions.

## Important Dependencies
- `Packet.h`
- `ItemInstance.h`
- `PacketListener.h`

[Category: Networking, UI]

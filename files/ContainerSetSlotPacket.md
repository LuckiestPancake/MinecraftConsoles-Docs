# ContainerSetSlotPacket

## Purpose
Updates the item content of a single specific slot within an open container or the player's inventory.

## Key Classes
- **ContainerSetSlotPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes the `containerId`, the `slot` index, and the `ItemInstance` data.
- `write()`: Encodes the slot update.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (103).

## Modding Notes
Used by the server to force an update to a specific slot on the client. If `containerId` is -1, it typically refers to the player's own inventory. This is more efficient than `ContainerSetContentPacket` when only one item changes.

## Important Dependencies
- `Packet.h`
- `ItemInstance.h`
- `PacketListener.h`

[Category: Networking, UI]

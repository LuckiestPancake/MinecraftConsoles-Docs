# TakeItemEntityPacket

## Purpose
The `TakeItemEntityPacket` is used to inform the client that an item entity has been picked up by a player. It triggers the visual animation of the item "flying" into the player's inventory.

## Key Classes
- **TakeItemEntityPacket**: The packet class for item pickup events.

## Important Functions
- **read(DataInputStream *dis)**: Reads the item entity ID and the player entity ID.
- **write(DataOutputStream *dos)**: Writes the item and player entity IDs.
- **handle(PacketListener *listener)**: Dispatches to `handleTakeItemEntity`.

## Modding Notes
- This packet does not handle the actual inventory change (that is done via `ContainerSetSlotPacket`), but rather handles the visual feedback.
- Categorized under **Entities** and **Networking**.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

---
**Related to:** [Entities](Entities.md), [Networking](Networking.md)

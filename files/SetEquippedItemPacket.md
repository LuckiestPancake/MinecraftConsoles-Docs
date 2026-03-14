# SetEquippedItemPacket

## Purpose
The `SetEquippedItemPacket` is used to synchronize the items equipped by an entity (such as weapons or armor) to all nearby clients.

## Key Classes
- `SetEquippedItemPacket`: The main class representing the packet.
- `ItemInstance`: Represents the equipped item.

## Important Functions
- `read(DataInputStream *dis)`: Reads the entity ID, slot index, and the item instance data.
- `write(DataOutputStream *dos)`: Writes the entity ID, slot index, and item data to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleSetEquippedItem` method.
- `getId()`: Returns the packet ID, which is 5.

## Modding Notes
- 4J Studios modified this packet to include the full `ItemInstance` data (bringing it forward from Minecraft 1.3) to fix an issue where enchanted item auras were not displaying for other players.
- Slot indices correspond to the entity's equipment slots (e.g., main hand, armor slots).

## Important Dependencies
- `Packet.h`
- `ItemInstance.h`
- `PacketListener.h`

Cross-references: Entities, Rendering.

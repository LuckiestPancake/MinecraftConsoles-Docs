# RemoveEntitiesPacket

## Purpose
The `RemoveEntitiesPacket` informs clients to remove one or more entities from their local world state.

## Key Classes
- `RemoveEntitiesPacket`: The main class representing the packet.
- `intArray`: A container for the list of entity IDs to be removed.

## Important Functions
- `read(DataInputStream *dis)`: Reads the number of entities and then reads each entity ID as an integer.
- `write(DataOutputStream *dos)`: Writes the entity count and the list of IDs to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleRemoveEntity` method.
- `getId()`: Returns the packet ID, which is 29.

## Modding Notes
- This packet can remove multiple entities in a single transmission, up to `MAX_PER_PACKET` (255).
- It is commonly used when entities despawn, are killed, or move out of the player's tracking range.

## Important Dependencies
- `Packet.h`
- `BasicTypeContainers.h`
- `PacketListener.h`

Cross-references: Entities.

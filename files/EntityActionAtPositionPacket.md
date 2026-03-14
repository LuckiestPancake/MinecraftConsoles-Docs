# EntityActionAtPositionPacket

## Purpose
The `EntityActionAtPositionPacket` is used to communicate specific actions performed by an entity at a given coordinate. It is commonly used for actions like starting to sleep.

## Key Classes
- `EntityActionAtPositionPacket`: The main class representing the packet.
- `Entity`: The entity performing the action.

## Important Functions
- `read(DataInputStream *dis)`: Reads the entity ID, action byte, and X, Y, Z coordinates.
- `write(DataOutputStream *dos)`: Writes the entity ID, action byte, and X, Y, Z coordinates.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleEntityActionAtPosition` method.
- `getId()`: Returns the packet ID, which is 17.

## Modding Notes
- This packet is specifically useful for actions that are tied to a location, such as interacting with a bed (sleeping).
- The `action` field defines what the entity is doing.

## Important Dependencies
- `Packet.h`
- `Entity.h`
- `PacketListener.h`

Cross-references: Entities, Movement.

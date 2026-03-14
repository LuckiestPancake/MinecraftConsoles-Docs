# SetEntityLinkPacket

## Purpose
The `SetEntityLinkPacket` is used to create or remove a link between two entities, specifically for mechanics like riding or leashing.

## Key Classes
- `SetEntityLinkPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the source entity ID, destination entity ID, and the link type byte.
- `write(DataOutputStream *dos)`: Writes the IDs and link type to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleEntityLinkPacket` method.
- `getId()`: Returns the packet ID, which is 39.

## Modding Notes
- Link types are `RIDING` (0) and `LEASH` (1).
- Setting the destination ID to -1 indicates that the link should be removed.
- This packet replaces the older `SetRidingPacket` for more generic entity linking.

## Important Dependencies
- `Packet.h`
- `Entity.h`
- `PacketListener.h`

Cross-references: Entities.

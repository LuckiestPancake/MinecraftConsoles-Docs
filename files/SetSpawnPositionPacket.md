# SetSpawnPositionPacket

## Purpose
The `SetSpawnPositionPacket` communicates the world's spawn point coordinates to the client. This affects where the player respawns if they don't have a bed and where the compass points.

## Key Classes
- **SetSpawnPositionPacket**: Packet containing X, Y, and Z coordinates for the spawn point.

## Important Functions
- **read(DataInputStream *dis)**: Reads three integers representing the X, Y, and Z coordinates.
- **write(DataOutputStream *dos)**: Writes the coordinates to the stream.
- **handle(PacketListener *listener)**: Dispatches to `handleSetSpawn`.
- **isInvalidatedBy(shared_ptr<Packet> packet)**: Any new spawn position packet invalidates the previous one.

## Modding Notes
- This packet is usually sent upon joining the world or when the spawn point is changed (e.g., via commands).
- It is categorized under **Movement** and **Networking**.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

---
**Related to:** [Movement](Movement.md), [Networking](Networking.md)

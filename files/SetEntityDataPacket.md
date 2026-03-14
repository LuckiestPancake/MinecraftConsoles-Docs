# SetEntityDataPacket

## Purpose
The `SetEntityDataPacket` is used to synchronize an entity's metadata (SynchedEntityData) with clients. This includes state flags, health, name tags, and other entity-specific data.

## Key Classes
- `SetEntityDataPacket`: The main class representing the packet.
- `SynchedEntityData`: The system managing the entity's synchronized data points.

## Important Functions
- `read(DataInputStream *dis)`: Reads the entity ID and unpacks the metadata items from the stream.
- `write(DataOutputStream *dos)`: Writes the entity ID and packs the metadata items into the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleSetEntityData` method.
- `getId()`: Returns the packet ID, which is 40.

## Modding Notes
- This packet is highly efficient as it can be configured to only send "dirty" (changed) data points rather than the entire metadata set.
- It is the primary way that visual states (like being on fire or sneaking) are synced for non-player entities.

## Important Dependencies
- `Packet.h`
- `SynchedEntityData.h`
- `PacketListener.h`

Cross-references: Entities.

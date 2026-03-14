# MoveEntityPacket

## Purpose
The `MoveEntityPacket` and its sub-classes are used to sync the movement and rotation of entities between the server and clients.

## Key Classes
- `MoveEntityPacket`: Base class for entity movement.
- `MoveEntityPacket::Pos`: Sub-class for relative position changes only.
- `MoveEntityPacket::Rot`: Sub-class for rotation changes only.
- `MoveEntityPacket::PosRot`: Sub-class for both position and rotation changes.

## Important Functions
- `read(DataInputStream *dis)`: Reads the entity ID and any relevant movement/rotation bytes.
- `write(DataOutputStream *dos)`: Writes the entity ID and movement/rotation data.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleMoveEntity` method.
- `getId()`: Returns 30 for the base, 31 for `Pos`, 32 for `Rot`, and 33 for `PosRot`.

## Modding Notes
- Movement data (`xa`, `ya`, `za`) is sent as relative bytes rather than absolute coordinates to save bandwidth.
- These packets are among the most frequently sent during gameplay to maintain smooth entity synchronization.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Entities, Movement.

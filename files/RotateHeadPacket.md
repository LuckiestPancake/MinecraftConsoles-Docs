# RotateHeadPacket

## Purpose
The `RotateHeadPacket` is used to synchronize the head rotation (yaw) of an entity, allowing players to see where other entities are looking independently of their body orientation.

## Key Classes
- `RotateHeadPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the entity ID and the head rotation byte (`yHeadRot`).
- `write(DataOutputStream *dos)`: Writes the entity ID and rotation byte to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleRotateMob` method.
- `getId()`: Returns the packet ID, which is 35.

## Modding Notes
- This packet is marked as `isAync()`, allowing it to be processed outside the main tick loop for smoother visual updates.
- It can be invalidated by subsequent `RotateHeadPacket` calls for the same entity to reduce network traffic.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Entities, Movement.

# MoveEntityPacketSmall

## Purpose
The `MoveEntityPacketSmall` is an optimized version of the entity movement packet, using bit-packing to reduce the size of the data sent for small relative movements and rotations.

## Key Classes
- `MoveEntityPacketSmall`: Base class for optimized entity movement.
- `MoveEntityPacketSmall::Pos`: Sub-class for packed relative position changes.
- `MoveEntityPacketSmall::Rot`: Sub-class for packed rotation changes.
- `MoveEntityPacketSmall::PosRot`: Sub-class for packed position and rotation changes.

## Important Functions
- `read(DataInputStream *dis)`: Reads bit-packed movement and rotation data.
- `write(DataOutputStream *dos)`: Writes bit-packed data to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleMoveEntitySmall` method.
- `getId()`: Returns 162 for the base, 163 for `Pos`, 164 for `Rot`, and 165 for `PosRot`.

## Modding Notes
- This packet uses bitwise operations to pack entity IDs, positions, and rotations into fewer bytes than the standard `MoveEntityPacket`.
- For example, `PosRot` packs the ID and Y-rotation into a single short, and X, Y, Z offsets into another short.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Entities, Movement.

# MovePlayerPacket

## Purpose
The `MovePlayerPacket` is used to sync the player's position, rotation, and movement state (on ground, flying) between the client and server.

## Key Classes
- `MovePlayerPacket`: Base class for player movement.
- `MovePlayerPacket::Pos`: Sub-class for absolute position updates.
- `MovePlayerPacket::Rot`: Sub-class for rotation updates.
- `MovePlayerPacket::PosRot`: Sub-class for both position and rotation updates.

## Important Functions
- `read(DataInputStream *dis)`: Reads position (double), rotation (float), and status flags (onGround, isFlying).
- `write(DataOutputStream *dos)`: Writes position, rotation, and status flags to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleMovePlayer` method.
- `getId()`: Returns 10 for the base, 11 for `Pos`, 12 for `Rot`, and 13 for `PosRot`.

## Modding Notes
- Unlike entity movement packets which are relative, player movement packets typically send absolute coordinates.
- The `isFlying` flag is a 4J Studios addition to the standard packet structure.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Movement.

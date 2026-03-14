# SetEntityMotionPacket

## Purpose
The `SetEntityMotionPacket` synchronizes an entity's velocity (motion vector) from the server to the clients.

## Key Classes
- `SetEntityMotionPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the entity ID and velocity components (X, Y, Z). It handles both the short and packed byte formats.
- `write(DataOutputStream *dos)`: Writes the ID and velocity to the stream, using the most efficient format available.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleSetEntityMotion` method.
- `getId()`: Returns the packet ID, which is 28.

## Modding Notes
- 4J Studios optimized this packet to use bytes instead of shorts for velocity if the values are within a specific range, significantly reducing bandwidth for small motions.
- Velocities are scaled by 8000.0 before being sent as shorts.

## Important Dependencies
- `Packet.h`
- `Entity.h`
- `PacketListener.h`

Cross-references: Entities, Movement.

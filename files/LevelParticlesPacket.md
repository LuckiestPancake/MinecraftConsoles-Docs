# LevelParticlesPacket

## Purpose
The `LevelParticlesPacket` is used to spawn particles in the world with specific spread and speed parameters.

## Key Classes
- `LevelParticlesPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the particle name, location (X, Y, Z), distribution area (xDist, yDist, zDist), maximum speed, and particle count.
- `write(DataOutputStream *dos)`: Writes the particle parameters to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleParticleEvent` method.
- `getId()`: Returns the packet ID, which is 63.

## Modding Notes
- This packet allows for precise control over particle effects, including their name (e.g., "smoke", "flame") and how they are dispersed.
- The `count` parameter specifies how many particles to spawn in a single call.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Rendering.

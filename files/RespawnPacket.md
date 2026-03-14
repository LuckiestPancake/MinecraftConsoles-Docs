# RespawnPacket

## Purpose
The `RespawnPacket` is sent by the server to a client when they respawn or change dimensions. It resets the player's state and provides updated world parameters.

## Key Classes
- `RespawnPacket`: The main class representing the packet.
- `GameType`: Defines the player's game mode (survival, creative, etc.).
- `LevelType`: Defines the world generator type.

## Important Functions
- `read(DataInputStream *dis)`: Reads the dimension ID, game mode, map height, level type name, map seed, difficulty, sea level flag, and new entity ID.
- `write(DataOutputStream *dos)`: Writes the respawn parameters to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleRespawn` method.
- `getId()`: Returns the packet ID, which is 9.

## Modding Notes
- 4J Studios added `m_newSeaLevel`, `m_newEntityId`, `m_xzSize`, and `m_hellScale` to support console-specific features and larger worlds.
- This packet is essential for clean transitions between the Overworld, Nether, and The End.

## Important Dependencies
- `Packet.h`
- `GameType.h`
- `LevelType.h`
- `PacketListener.h`

Cross-references: Networking.

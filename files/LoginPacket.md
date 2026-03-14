# LoginPacket

## Purpose
The `LoginPacket` is the primary packet used for the initial handshake when a player joins a server. it transmits essential information about the player and the world they are entering.

## Key Classes
- `LoginPacket`: The main class representing the packet.
- `LevelType`: Defines the type of world (e.g., flat, normal).

## Important Functions
- `read(DataInputStream *dis)`: Reads comprehensive player and world data including client version, username, world seed, dimension, difficulty, and 4J-specific metadata like XUIDs and skin IDs.
- `write(DataOutputStream *dos)`: Writes all session and player data to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleLogin` method.
- `getId()`: Returns the packet ID, which is 1.

## Modding Notes
- This packet is highly modified by 4J Studios to include console-specific features like multiplayer instance IDs, player indices, and guest status.
- It contains world-generation settings like `xzSize` and `hellScale` for large worlds.

## Important Dependencies
- `Packet.h`
- `LevelType.h`
- `PacketListener.h`

Cross-references: Networking.

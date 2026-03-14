# PlayerInfoPacket

## Purpose
The `PlayerInfoPacket` is used to synchronize player-specific metadata, such as network IDs, color indices, and game privileges, between the server and all connected clients.

## Key Classes
- `PlayerInfoPacket`: The main class representing the packet.
- `ServerPlayer`: The server-side representation of a player.

## Important Functions
- `read(DataInputStream *dis)`: Reads the network small ID, player color index, privileges bitfield, and entity ID.
- `write(DataOutputStream *dos)`: Writes the player info to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handlePlayerInfo` method.
- `getId()`: Returns the packet ID, which is 201.

## Modding Notes
- 4J Studios significantly repurposed this packet from its original Java version to include console-specific features like player color indices and game privileges.
- The `m_networkSmallId` is used for efficient network identification.

## Important Dependencies
- `Packet.h`
- `ServerPlayer.h`
- `PacketListener.h`

Cross-references: Networking.

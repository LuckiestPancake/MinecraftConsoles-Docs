# PreLoginPacket

## Purpose
The `PreLoginPacket` is the initial handshake packet sent when a client attempts to connect to a server. It contains vital information for validating the connection and setting up the session.

## Key Classes
- `PreLoginPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the netcode version, username (login key), UGC privileges, XUIDs for all local players, server settings bitfield, and texture pack ID.
- `write(DataOutputStream *dos)`: Writes the pre-login data to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handlePreLogin` method.
- `getId()`: Returns the packet ID, which is 2.

## Modding Notes
- This packet handles console-specific User Generated Content (UGC) privileges to ensure players can join sessions based on their privacy settings.
- It also synchronizes the `texturePackId` to ensure the client is using the correct assets.
- The `m_szUniqueSaveName` is used for ban list verification.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Networking.

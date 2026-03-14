# ClientProtocolPacket

## Purpose
Originally designed for the initial handshake between client and server to verify protocol versions and exchange basic user information.

## Key Classes
- **ClientProtocolPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes protocol version, username, hostname, and port (commented out).
- `write()`: Encodes the handshake data (commented out).
- `handle()`: Dispatches to `handleClientProtocolPacket` (commented out).

## Modding Notes
This packet is not used in the LuckysConsoleEdition codebase and is `#if 0`'d out. Handshaking and initial login data are instead handled by the 4J-specific `PreLoginPacket` (ID 2).

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking]

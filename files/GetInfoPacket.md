# GetInfoPacket

## Purpose
The `GetInfoPacket` is a small, empty packet used to request basic server information, typically used by the client when pinging a server in the server list.

## Key Classes
- `GetInfoPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: No data to read.
- `write(DataOutputStream *dos)`: No data to write.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleGetInfo` method.
- `getId()`: Returns the packet ID, which is 254.

## Modding Notes
- This packet has an estimated size of 0 as it carries no payload beyond the packet ID.
- It is primarily used for server discovery and status pings.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Networking.

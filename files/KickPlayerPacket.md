# KickPlayerPacket

## Purpose
The `KickPlayerPacket` is used by the server to forcefully disconnect a specific player from the game session.

## Key Classes
- `KickPlayerPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the `networkSmallId` of the player to be kicked.
- `write(DataOutputStream *dos)`: Writes the `networkSmallId` of the player to be kicked.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleKickPlayer` method.
- `getId()`: Returns the packet ID, which is 159.

## Modding Notes
- This is a administrative packet used for session management.
- Unlike `DisconnectPacket`, which informs the receiver they are being disconnected, `KickPlayerPacket` is often used internally to manage remote connections.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Networking.

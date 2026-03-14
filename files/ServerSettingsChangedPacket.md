# ServerSettingsChangedPacket

## Purpose
The `ServerSettingsChangedPacket` is a 4J Studios-specific packet used to synchronize changes in host settings (like difficulty or game options) to all clients in the session.

## Key Classes
- `ServerSettingsChangedPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the action byte and a data integer.
- `write(DataOutputStream *dos)`: Writes the action and data to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleServerSettingsChanged` method.
- `getId()`: Returns the packet ID, which is 153.

## Modding Notes
- Actions include `HOST_DIFFICULTY` (0), `HOST_OPTIONS` (1), and `HOST_IN_GAME_SETTINGS` (2).
- This packet ensures that all players are aware of real-time configuration changes made by the host.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Networking.

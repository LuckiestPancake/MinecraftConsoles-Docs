# SetPlayerTeamPacket

## Purpose
The `SetPlayerTeamPacket` is a comprehensive packet for managing scoreboard teams and their memberships.

## Key Classes
- `SetPlayerTeamPacket`: The main class representing the packet.
- `PlayerTeam`: The team being modified.

## Important Functions
- `read(DataInputStream *dis)`: Reads the team name, method, and (depending on the method) display name, prefix, suffix, options, and a list of player names.
- `write(DataOutputStream *dos)`: Writes the team configuration or membership changes to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleSetPlayerTeamPacket` method.
- `getId()`: Returns the packet ID, which is 209.

## Modding Notes
- Supported methods: `METHOD_ADD` (0), `METHOD_REMOVE` (1), `METHOD_CHANGE` (2), `METHOD_JOIN` (3), `METHOD_LEAVE` (4).
- The `options` field contains packed team settings like friendly fire and name tag visibility.

## Important Dependencies
- `Packet.h`
- `PlayerTeam.h`
- `PacketListener.h`

Cross-references: UI.

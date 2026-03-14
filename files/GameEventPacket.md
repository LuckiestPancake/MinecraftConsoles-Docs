# GameEventPacket

## Purpose
The `GameEventPacket` is used to trigger various predefined game events on the client, such as changing the weather, updating the game mode, or signaling a successful bow hit.

## Key Classes
- `GameEventPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the event ID and a parameter byte.
- `write(DataOutputStream *dos)`: Writes the event ID and a parameter byte.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleGameEvent` method.
- `getId()`: Returns the packet ID, which is 70.

## Modding Notes
- Common event constants include `START_RAINING`, `STOP_RAINING`, `CHANGE_GAME_MODE`, and `WIN_GAME`.
- 4J Studios added specific events for `START_SAVING` and `STOP_SAVING`.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Networking.

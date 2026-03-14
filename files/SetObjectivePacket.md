# SetObjectivePacket

## Purpose
The `SetObjectivePacket` is used to manage scoreboard objectives, allowing the server to add, remove, or update objectives on the client.

## Key Classes
- `SetObjectivePacket`: The main class representing the packet.
- `Objective`: The scoreboard objective being modified.

## Important Functions
- `read(DataInputStream *dis)`: Reads the objective name, display name, and the method (add/remove/change).
- `write(DataOutputStream *dos)`: Writes the objective data to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleAddObjective` method.
- `getId()`: Returns the packet ID, which is 206.

## Modding Notes
- Methods are `METHOD_ADD` (0), `METHOD_REMOVE` (1), and `METHOD_CHANGE` (2).
- The `objectiveName` is the internal identifier, while `displayName` is what appears to the user.

## Important Dependencies
- `Packet.h`
- `Objective.h`
- `PacketListener.h`

Cross-references: UI.

# SetDisplayObjectivePacket

## Purpose
The `SetDisplayObjectivePacket` is used to specify which scoreboard objective should be displayed in a particular display slot (e.g., list, sidebar, or below name).

## Key Classes
- `SetDisplayObjectivePacket`: The main class representing the packet.
- `Objective`: The scoreboard objective to be displayed.

## Important Functions
- `read(DataInputStream *dis)`: Reads the display slot byte and the objective name (UTF string).
- `write(DataOutputStream *dos)`: Writes the slot and objective name to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleSetDisplayObjective` method.
- `getId()`: Returns the packet ID, which is 208.

## Modding Notes
- Sending an empty objective name effectively clears the display for that slot.
- Display slots are usually 0 (list), 1 (sidebar), and 2 (below name).

## Important Dependencies
- `Packet.h`
- `Objective.h`
- `PacketListener.h`

Cross-references: UI.

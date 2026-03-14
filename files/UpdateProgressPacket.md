# UpdateProgressPacket

## Purpose
The `UpdateProgressPacket` is a 4J-specific packet used to communicate a simple percentage completion of a background task (such as world saving or loading) to the client.

## Key Classes
- **UpdateProgressPacket**: The packet class for progress percentages.

## Important Functions
- **read(DataInputStream *dis)**: Reads a single byte representing the percentage (0-100).
- **write(DataOutputStream *dos)**: Writes the percentage byte.
- **handle(PacketListener *listener)**: Dispatches to `handleUpdateProgress`.

## Modding Notes
- This is primarily used for the progress bar shown during long operations on the console.
- Categorized under **UI** and **Networking**.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

---
**Related to:** [UI](UI.md), [Networking](Networking.md)

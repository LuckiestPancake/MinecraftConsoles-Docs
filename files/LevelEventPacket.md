# LevelEventPacket

## Purpose
The `LevelEventPacket` is used to trigger specific effects or events at a location in the world, such as block breaking particles, fire extinguishing sounds, or other environment-related events.

## Key Classes
- `LevelEventPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the event type, X, Y, Z coordinates, event-specific data, and whether it is a global event.
- `write(DataOutputStream *dos)`: Writes the event data to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleLevelEvent` method.
- `getId()`: Returns the packet ID, which is 61.

## Modding Notes
- The `type` field determines what effect is played.
- `data` is used for event-specific information (e.g., the block ID for a break effect).
- Global events are heard by all players regardless of distance.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Networking.

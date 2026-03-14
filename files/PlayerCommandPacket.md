# PlayerCommandPacket

## Purpose
The `PlayerCommandPacket` is used to communicate state changes of the player entity that aren't direct movement, such as sneaking, sprinting, or jumping while riding.

## Key Classes
- `PlayerCommandPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the entity ID, action ID, and an auxiliary data integer.
- `write(DataOutputStream *dos)`: Writes the entity ID, action ID, and data to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handlePlayerCommand` method.
- `getId()`: Returns the packet ID, which is 19.

## Modding Notes
- Actions include `START_SNEAKING` (1), `STOP_SNEAKING` (2), `STOP_SLEEPING` (3), `START_SPRINTING` (4), `STOP_SPRINTING` (5), `RIDING_JUMP` (8), and `OPEN_INVENTORY` (9).
- `START_IDLEANIM` and `STOP_IDLEANIM` are also supported (IDs 6 and 7).

## Important Dependencies
- `Packet.h`
- `Entity.h`
- `PacketListener.h`

Cross-references: Movement.

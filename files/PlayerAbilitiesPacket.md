# PlayerAbilitiesPacket

## Purpose
The `PlayerAbilitiesPacket` synchronizes the player's special abilities and movement speeds between the server and client.

## Key Classes
- `PlayerAbilitiesPacket`: The main class representing the packet.
- `Abilities`: The underlying class containing the player's ability states.

## Important Functions
- `read(DataInputStream *dis)`: Reads a bitfield of flags (invulnerable, flying, canFly, instabuild) and floating-point values for flying and walking speeds.
- `write(DataOutputStream *dos)`: Writes the bitfield and speed values to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handlePlayerAbilities` method.
- `getId()`: Returns the packet ID, which is 202.

## Modding Notes
- Flags are packed into a single byte using bitwise operations (`1 << 0` for invulnerable, etc.).
- This packet is critical for creative mode functionality and specialized player states in survival.

## Important Dependencies
- `Packet.h`
- `Abilities.h`
- `PacketListener.h`

Cross-references: Networking.

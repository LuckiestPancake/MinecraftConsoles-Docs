# AddExperienceOrbPacket

## Purpose
A network packet used to notify clients that an experience orb has been spawned in the world.

## Key Classes
- **AddExperienceOrbPacket**: Inherits from `Packet` to communicate experience orb spawning.

## Important Functions
- `read()`: Reads entity ID, position, and experience value.
- `write()`: Writes entity ID, position, and experience value.
- `handle()`: Dispatches to `PacketListener`.
- `getId()`: Returns the packet ID (26).

## Modding Notes
The position is encoded using fixed-point math (multiplied by 32).

## Important Dependencies
- `Packet.h`
- `ExperienceOrb.h`

[Category: Networking]

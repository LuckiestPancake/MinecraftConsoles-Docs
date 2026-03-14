# AnimatePacket

## Purpose
A network packet used to trigger various animations on an entity, such as swinging an arm, taking damage, or eating.

## Key Classes
- **AnimatePacket**: Inherits from `Packet`.

## Important Functions
- `SWING`, `HURT`, `WAKE_UP`, `RESPAWN`, `EAT`, `CRITICAL_HIT`, `MAGIC_CRITICAL_HIT`: Constants for different animation types.
- `read()`/`write()`: Handles entity ID and action byte.
- `handle()`: Dispatches to `PacketListener`.

## Modding Notes
The `EAT` action (5) was added in version 1.8.2 of the game.

## Important Dependencies
- `Packet.h`
- `Entity.h`

[Category: Networking]

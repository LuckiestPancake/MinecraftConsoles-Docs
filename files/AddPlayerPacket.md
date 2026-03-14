# AddPlayerPacket

## Purpose
A network packet sent to notify clients that a player has joined the world or entered their tracking range. It contains extensive player-specific data including skin/cape IDs and game privileges.

## Key Classes
- **AddPlayerPacket**: Inherits from `Packet` for player spawning.

## Important Functions
- `read()`/`write()`: Handles player name, position, rotations, held item, XUIDs (4J unique), skin IDs, and privileges.
- `handle()`: Dispatches to `PacketListener`.

## Modding Notes
4J Studios added many console-specific fields: `xuid`, `OnlineXuid`, `m_playerIndex`, `m_skinId`, `m_capeId`, and `m_uiGamePrivileges`. These are critical for the console edition's social and identity features.

## Important Dependencies
- `Packet.h`
- `Player.h`
- `SynchedEntityData.h`

[Category: Networking]

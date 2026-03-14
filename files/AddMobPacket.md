# AddMobPacket

## Purpose
A network packet sent by the server to clients to spawn a living entity (mob) in the world. It carries position, rotation, velocity, and initial metadata (SynchedEntityData).

## Key Classes
- **AddMobPacket**: Inherits from `Packet` for mob spawning.

## Important Functions
- `read()`/`write()`: Handles serialization of mob data, including rotations and entity metadata.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getUnpackedData()`: Provides access to the mob's metadata for client-side initialization.

## Modding Notes
Similar to `AddEntityPacket`, it supports `_LARGE_WORLDS` with 32-bit coordinates. It also handles head rotation (`yHeadRot`), which is separate from body rotation.

## Important Dependencies
- `Packet.h`
- `SynchedEntityData.h`
- `LivingEntity.h`

[Category: Networking]

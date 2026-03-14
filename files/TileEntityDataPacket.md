# TileEntityDataPacket

## Purpose
The `TileEntityDataPacket` is used to synchronize the state (NBT data) of a tile entity (e.g., Mob Spawner, Beacon, Skull) from the server to the client.

## Key Classes
- **TileEntityDataPacket**: The packet class for tile entity synchronization.
- **CompoundTag**: Represents the NBT data of the tile entity.

## Important Functions
- **read(DataInputStream *dis)**: Reads the coordinates, type, and the NBT data using `readNbt`.
- **write(DataOutputStream *dos)**: Writes the tile entity data using `writeNbt`.
- **handle(PacketListener *listener)**: Dispatches to `handleTileEntityData`.

## Modding Notes
- Common types: `TYPE_MOB_SPAWNER (1)`, `TYPE_ADV_COMMAND (2)`, `TYPE_BEACON (3)`, `TYPE_SKULL (4)`.
- This packet is essential for ensuring clients see the correct configuration of complex blocks.
- Categorized under **Entities** (Tile Entities) and **Networking**.

## Important Dependencies
- `Packet.h`
- `CompoundTag.h` (NBT)

---
**Related to:** [Entities](Entities.md), [Networking](Networking.md)

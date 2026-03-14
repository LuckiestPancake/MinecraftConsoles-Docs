# TileEventPacket

## Purpose
The `TileEventPacket` is used for block-specific events that trigger visual or sound effects, such as a chest opening, a piston moving, or a note block playing.

## Key Classes
- **TileEventPacket**: The packet class for block events.

## Important Functions
- **read(DataInputStream *dis)**: Reads coordinates, two generic parameter bytes (`b0`, `b1`), and the block type.
- **write(DataOutputStream *dos)**: Writes the event data.
- **handle(PacketListener *listener)**: Dispatches to `handleTileEvent`.

## Modding Notes
- The meaning of `b0` and `b1` depends entirely on the block ID. For example, for a chest, `b0` might be 1 for opening and 0 for closing.
- Categorized under **Entities** (Tile Entities), **Rendering**, and **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.world.level.tile.h`

---
**Related to:** [Entities](Entities.md), [Rendering](Rendering.md), [Networking](Networking.md)

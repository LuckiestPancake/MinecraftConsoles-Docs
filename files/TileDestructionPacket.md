# TileDestructionPacket

## Purpose
The `TileDestructionPacket` is used to synchronize block breaking progress (the "cracks" shown on blocks) across clients.

## Key Classes
- **TileDestructionPacket**: The packet class for block damage updates.

## Important Functions
- **read(DataInputStream *dis)**: Reads the breaking entity's ID, the block coordinates, and the destruction state.
- **write(DataOutputStream *dos)**: Writes the destruction data.
- **handle(PacketListener *listener)**: Dispatches to `handleTileDestruction`.

## Modding Notes
- The `state` is an unsigned byte, typically ranging from 0 to 9, representing the visual crack level.
- Categorized under **Rendering** and **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.network.packet.h`

---
**Related to:** [Rendering](Rendering.md), [Networking](Networking.md)

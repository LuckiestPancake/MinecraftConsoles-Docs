# UseItemPacket

## Purpose
The `UseItemPacket` is sent by the client to the server when a player interacts with a block using an item. It provides precise details about where and how the block was clicked.

## Key Classes
- **UseItemPacket**: The packet class for item usage events.
- **ItemInstance**: The item that was held when the interaction occurred.

## Important Functions
- **read(DataInputStream *dis)**: Reads coordinates, block face, item data, and precise click offsets (`clickX`, `clickY`, `clickZ`).
- **write(DataOutputStream *dos)**: Writes the interaction details.
- **handle(PacketListener *listener)**: Dispatches to `handleUseItem`.

## Modding Notes
- `CLICK_ACCURACY` (16.0f) is used to compress floating-point click offsets into single bytes.
- This packet is critical for placing blocks or using tools on blocks.
- Categorized under **Movement** (Interactions) and **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.world.item.h`

---
**Related to:** [Movement](Movement.md), [Networking](Networking.md)

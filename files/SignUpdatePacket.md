# SignUpdatePacket

## Purpose
The `SignUpdatePacket` is used to transmit the text content of a sign at a specific coordinate. It is sent when a player finishes editing a sign or when a sign is loaded for the client.

## Key Classes
- **SignUpdatePacket**: Packet containing the sign's position and its 4 lines of text.
- **SignTileEntity**: The tile entity associated with the sign.

## Important Functions
- **read(DataInputStream *dis)**: Reads coordinates, verification/censorship flags, and the 4 lines of UTF-8 text.
- **write(DataOutputStream *dos)**: Writes the sign data to the stream.
- **handle(PacketListener *listener)**: Dispatches to `handleSignUpdate`.

## Modding Notes
- 4J Specifics: Includes `m_bVerified` and `m_bCensored` flags, likely for platform-specific content filtering.
- Uses `MAX_SIGN_LINES` (usually 4) and `SignTileEntity::MAX_LINE_LENGTH`.
- Categorized under **Entities** (Tile Entities), **UI**, and **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.world.level.tile.entity.h`
- `PacketListener.h`

---
**Related to:** [Entities](Entities.md), [UI](UI.md), [Networking](Networking.md)

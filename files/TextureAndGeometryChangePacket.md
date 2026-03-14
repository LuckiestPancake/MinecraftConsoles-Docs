# TextureAndGeometryChangePacket

## Purpose
The `TextureAndGeometryChangePacket` is a 4J-specific packet used to signal a change in both the texture and the geometric model (skin) of an entity.

## Key Classes
- **TextureAndGeometryChangePacket**: Packet class for skin/model changes.
- **Entity**: The entity whose appearance is changing.

## Important Functions
- **TextureAndGeometryChangePacket(shared_ptr<Entity> e, const wstring &path)**: Constructor that parses a skin ID from a file path and applies a bitmask.
- **read(DataInputStream *dis)**: Reads entity ID, skin ID, and the path string.
- **write(DataOutputStream *dos)**: Writes the change data to the stream.

## Modding Notes
- This packet uses `MAKE_SKIN_BITMASK` and parses the skin ID from the string (e.g., from `skins/123.png` it would extract `123`).
- Categorized under **Rendering**, **Entities**, and **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.world.entity.h`

---
**Related to:** [Rendering](Rendering.md), [Entities](Entities.md), [Networking](Networking.md)

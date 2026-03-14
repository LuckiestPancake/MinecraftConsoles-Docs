# TextureChangePacket

## Purpose
The `TextureChangePacket` is used to update the skin or cape texture of an entity by providing a path to the new texture.

## Key Classes
- **TextureChangePacket**: Packet for skin/cape path updates.

## Important Functions
- **read(DataInputStream *dis)**: Reads the entity ID, the action type (Skin or Cape), and the path string.
- **write(DataOutputStream *dos)**: Writes the update data.

## Modding Notes
- `ETextureChangeType` defines two actions: `e_TextureChange_Skin (0)` and `e_TextureChange_Cape (1)`.
- Categorized under **Rendering**, **Entities**, and **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.world.entity.h`

---
**Related to:** [Rendering](Rendering.md), [Entities](Entities.md), [Networking](Networking.md)

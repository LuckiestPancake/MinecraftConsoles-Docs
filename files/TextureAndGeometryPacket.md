# TextureAndGeometryPacket

## Purpose
The `TextureAndGeometryPacket` is a 4J-specific packet used to send raw texture data and custom geometric "boxes" (for custom player models or DLC skins) to the client.

## Key Classes
- **TextureAndGeometryPacket**: The packet class carrying the raw data.
- **SKIN_BOX**: A structure defining a 3D part of a custom model (X, Y, Z, Width, Height, Depth, and UV coordinates).
- **DLCSkinFile**: Helper for managing skin data from DLC.

## Important Functions
- **read(DataInputStream *dis)**: Reads the texture name, raw pixel data (if present), animation override bitmask, and a list of `SKIN_BOX` objects.
- **write(DataOutputStream *dos)**: Writes the texture and geometry data.
- **getEstimatedSize()**: Returns a large value (4096+) due to the potentially large payload.

## Modding Notes
- This is a very powerful packet for custom character modeling and skinning in the console editions.
- It can transmit up to 65536 bytes of raw texture data.
- Categorized under **Rendering** and **Networking**.

## Important Dependencies
- `Packet.h`
- `..\Minecraft.Client\Model.h`
- `..\Minecraft.Client\SkinBox.h`

---
**Related to:** [Rendering](Rendering.md), [Networking](Networking.md)

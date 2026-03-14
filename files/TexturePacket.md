# TexturePacket

## Purpose
The `TexturePacket` is a 4J-specific packet used to transmit raw texture data (as a byte array) to the client, associated with a specific texture name.

## Key Classes
- **TexturePacket**: The packet class carrying the raw texture payload.

## Important Functions
- **read(DataInputStream *dis)**: Reads the texture name and up to 65536 bytes of raw data into a newly allocated buffer.
- **write(DataOutputStream *dos)**: Writes the texture name and data.
- **handle(PacketListener *listener)**: Dispatches to `handleTexture`.

## Modding Notes
- This packet is used for custom skins or other dynamic texture updates on the console edition.
- Categorized under **Rendering** and **Networking**.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

---
**Related to:** [Rendering](Rendering.md), [Networking](Networking.md)

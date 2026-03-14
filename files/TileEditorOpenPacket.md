# TileEditorOpenPacket

## Purpose
The `TileEditorOpenPacket` instructs the client to open a specific editor interface for a block, such as the sign text editor or the command block interface.

## Key Classes
- **TileEditorOpenPacket**: The packet class for opening block-specific GUIs.

## Important Functions
- **read(DataInputStream *dis)**: Reads the editor type and the block coordinates.
- **write(DataOutputStream *dos)**: Writes the data to the stream.
- **handle(PacketListener *listener)**: Dispatches to `handleTileEditorOpen`.

## Modding Notes
- `editorType` constants: `SIGN (0)` and `COMMAND_BLOCK (1)`.
- Categorized under **UI** and **Networking**.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

---
**Related to:** [UI](UI.md), [Networking](Networking.md)

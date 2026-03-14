# SetCarriedItemPacket

## Purpose
The `SetCarriedItemPacket` informs the server which inventory slot the player currently has selected in their hotbar.

## Key Classes
- `SetCarriedItemPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the selected slot index as a short.
- `write(DataOutputStream *dos)`: Writes the slot index to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleSetCarriedItem` method.
- `getId()`: Returns the packet ID, which is 16.

## Modding Notes
- This packet is critical for ensuring the server knows which item the player is holding for interaction and rendering purposes.
- It can be invalidated by newer `SetCarriedItemPacket` calls to avoid redundant updates.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: UI.

# PlayerActionPacket

## Purpose
The `PlayerActionPacket` is sent by the client to inform the server of actions performed by the player on blocks or items, such as starting to dig, dropping an item, or releasing a used item.

## Key Classes
- `PlayerActionPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the action ID, block coordinates (X, Y, Z), and the face of the block being acted upon.
- `write(DataOutputStream *dos)`: Writes the action ID, coordinates, and face to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handlePlayerAction` method.
- `getId()`: Returns the packet ID, which is 14.

## Modding Notes
- Action IDs include `START_DESTROY_BLOCK` (0), `ABORT_DESTROY_BLOCK` (1), `STOP_DESTROY_BLOCK` (2), `DROP_ALL_ITEMS` (3), `DROP_ITEM` (4), and `RELEASE_USE_ITEM` (5).
- This packet is essential for block mining logic and inventory management.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Movement.

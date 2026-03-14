# SetCreativeModeSlotPacket

## Purpose
The `SetCreativeModeSlotPacket` is used by players in creative mode to set the contents of a specific inventory slot.

## Key Classes
- `SetCreativeModeSlotPacket`: The main class representing the packet.
- `ItemInstance`: Represents the item being placed in the slot.

## Important Functions
- `read(DataInputStream *dis)`: Reads the slot number (short) and the item instance data.
- `write(DataOutputStream *dos)`: Writes the slot number and item data to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleSetCreativeModeSlot` method.
- `getId()`: Returns the packet ID, which is 107.

## Modding Notes
- This packet is only relevant when the player is in creative mode and interacts with the creative inventory.
- 4J Studios ensures the packet takes a copy of the item instance to maintain data ownership.

## Important Dependencies
- `Packet.h`
- `ItemInstance.h`
- `PacketListener.h`

Cross-references: UI.

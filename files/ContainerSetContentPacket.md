# ContainerSetContentPacket

## Purpose
Synchronizes the entire contents of a container from the server to the client. This is used when a container is first opened or when a major update occurs that affects all slots.

## Key Classes
- **ContainerSetContentPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes the container ID and the array of `ItemInstance` objects.
- `write()`: Encodes the list of items for the client.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (104).

## Modding Notes
Uses `ItemInstanceArray` to handle a variable number of slots efficiently. This packet ensures that the client's visual representation of a chest or inventory perfectly matches the server's authoritative state.

## Important Dependencies
- `Packet.h`
- `ItemInstance.h`
- `PacketListener.h`

[Category: Networking, UI]

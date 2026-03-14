# ContainerAckPacket

## Purpose
Synchronizes container transactions between the client and server. It acknowledges whether a specific action (like moving an item) was successful, preventing synchronization issues.

## Key Classes
- **ContainerAckPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes the container ID, unique transaction ID (`uid`), and the acceptance status.
- `write()`: Encodes the acknowledgement.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (106).

## Modding Notes
This packet is a critical component of the inventory system's reliability. By using a unique transaction ID, it ensures that even with network latency, the client and server agree on the state of the player's inventory and any open containers.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking, UI]

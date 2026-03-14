# ContainerClosePacket

## Purpose
Informs the other side (usually server to client or vice-versa) that a container has been closed, allowing the associated resources and GUI to be cleaned up.

## Key Classes
- **ContainerClosePacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes the ID of the container being closed.
- `write()`: Encodes the `containerId`.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (101).

## Modding Notes
A straightforward packet used to maintain state. Closing a container on the client will send this to the server to ensure the server-side `Container` object is also closed and any "temporary" items are handled.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking, UI]

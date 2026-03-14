# ClientCommandPacket

## Purpose
A packet sent by the client to the server to perform specific meta-actions, primarily used for completing the login process or requesting a respawn after death.

## Key Classes
- **ClientCommandPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes the action ID from the network stream.
- `write()`: Encodes the action ID.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (205).

## Modding Notes
Defines two main constants: `LOGIN_COMPLETE` (0) and `PERFORM_RESPAWN` (1). This packet is essential for the state machine of the client-server connection, signaling when the client is ready to enter the world or wants to revive.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking]

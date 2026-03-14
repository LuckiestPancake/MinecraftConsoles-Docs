# DisconnectPacket

## Purpose
The `DisconnectPacket` is used to inform the client or server that a connection is being closed and provides a specific reason for the disconnection.

## Key Classes
- `DisconnectPacket`: The main class representing the packet, inheriting from `Packet`.
- `eDisconnectReason`: An enumeration defining various reasons for disconnection (e.g., quitting, kicked, server full, timeout, etc.).

## Important Functions
- `read(DataInputStream *dis)`: Reads the disconnection reason as an integer from the input stream.
- `write(DataOutputStream *dos)`: Writes the disconnection reason as an integer to the output stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleDisconnect` method.
- `getId()`: Returns the packet ID, which is 255.

## Modding Notes
- This packet is critical for handling clean exits and informing players why they were removed from a session.
- New disconnection reasons can be added to the `eDisconnectReason` enum to provide more granular feedback to users.

## Important Dependencies
- `Packet.h`
- `InputOutputStream.h`
- `PacketListener.h`

Cross-references: Networking.

# KeepAlivePacket

## Purpose
The `KeepAlivePacket` is used to maintain the connection between the client and server. It is sent periodically to ensure that the connection is still active and to measure latency.

## Key Classes
- `KeepAlivePacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the keep-alive ID.
- `write(DataOutputStream *dos)`: Writes the keep-alive ID.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleKeepAlive` method.
- `getId()`: Returns the packet ID, which is 0.

## Modding Notes
- This packet is marked as `isAync()`, meaning it can be handled outside the main game loop to ensure timely heartbeat responses.
- It can be invalidated by other packets to avoid redundant connection checks.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Networking.

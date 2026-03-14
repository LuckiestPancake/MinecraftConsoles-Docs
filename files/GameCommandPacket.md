# GameCommandPacket

## Purpose
The `GameCommandPacket` is a generic packet used to send various game-specific commands and their associated payloads between the client and server.

## Key Classes
- `GameCommandPacket`: The main class representing the packet.
- `EGameCommand`: An enumeration of available game commands.
- `byteArray`: A container for the command's payload data.

## Important Functions
- `read(DataInputStream *dis)`: Reads the command ID and the payload length, then reads the payload data.
- `write(DataOutputStream *dos)`: Writes the command ID, payload length, and the payload data.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleGameCommand` method.
- `getId()`: Returns the packet ID, which is 167.

## Modding Notes
- This packet acts as a flexible container for custom commands.
- The payload size is limited to 32KB.

## Important Dependencies
- `Packet.h`
- `CommandsEnum.h`
- `BasicTypeContainers.h`
- `PacketListener.h`

Cross-references: Networking.

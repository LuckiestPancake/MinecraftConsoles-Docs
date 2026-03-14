# ChatPacket

## Purpose
Handles the transmission of chat messages between the server and clients. This includes player-to-player communication, system notifications, and detailed death messages.

## Key Classes
- **ChatPacket**: Inherits from `Packet` to manage chat data.
- **EChatPacketMessage**: An enum defining a wide range of localized message types (e.g., bed status, death causes, entity limits, teleport success).

## Important Functions
- `read()`: Decodes the message type and arguments from the network stream.
- `write()`: Encodes the message type and arguments (strings and integers) for transmission.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (3).

## Modding Notes
4J Studios heavily extended this packet to support localized strings via the `EChatPacketMessage` enum. This allows the console to display messages in the user's language without sending the full translated text over the network. It also includes specific logic for entity limits (e.g., `e_ChatPlayerMaxAnimals`).

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking, UI]

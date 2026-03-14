# ChatAutoCompletePacket

## Purpose
A network packet intended to handle chat auto-completion suggestions. It was designed to send a partial message to the server or client to receive a list of possible completions.

## Key Classes
- **ChatAutoCompletePacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes packet data (message string) from a `DataInputStream`.
- `write()`: Encodes packet data to a `DataOutputStream`.
- `handle()`: Dispatches the packet to the `PacketListener` via `handleChatAutoComplete`.
- `getMessage()`: Returns the message string to be auto-completed.

## Modding Notes
This packet is currently commented out in the 4J Studios codebase (`Packet.cpp` and `ChatAutoCompletePacket.h`), suggesting it was either disabled or not fully implemented for this console version. It carries a placeholder ID of 203.

## Important Dependencies
- `Packet.h`
- `ChatPacket.h`
- `PacketListener.h`

[Category: Networking, UI]

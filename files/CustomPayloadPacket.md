# CustomPayloadPacket

## Purpose
A versatile packet used for "plugin channels," allowing the exchange of arbitrary data between client and server. It is used for both standard Minecraft features (like book signing) and potential mod-added features.

## Key Classes
- **CustomPayloadPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes the channel `identifier` string and the raw `byteArray` payload.
- `write()`: Encodes the custom payload.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (250).

## Modding Notes
Standard Mojang channels include `MC|BEdit` (editing a book), `MC|BSign` (signing a book), `MC|TrList` (villager trade list), and `MC|AdvCdm` (command block edits). The maximum length of the data depends on the specific channel implementation.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking]

# CraftItemPacket

## Purpose
A 4J Studios-specific packet used to handle item crafting operations. It signals the server to perform a craft using a specific recipe.

## Key Classes
- **CraftItemPacket**: Inherits from `Packet`.

## Important Functions
- `read()`: Decodes the `recipe` ID and the transaction `uid`.
- `write()`: Encodes the crafting request.
- `handle()`: Dispatches the packet to the `PacketListener`.
- `getId()`: Returns the packet ID (150).

## Modding Notes
This packet is an optimization for the Console Edition's recipe-based crafting system. Instead of the client manually moving items into a crafting grid (which would require multiple `ContainerClickPacket` calls), the client sends a single `CraftItemPacket` with the desired recipe ID, and the server handles the item consumption and output.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

[Category: Networking, UI]

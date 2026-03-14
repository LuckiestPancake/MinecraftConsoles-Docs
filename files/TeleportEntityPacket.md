# TeleportEntityPacket

## Purpose
The `TeleportEntityPacket` is used to forcefully update an entity's position and rotation on the client side. This is typically used for rapid movement or when an entity's position on the server has diverged significantly from the client's.

## Key Classes
- **TeleportEntityPacket**: The main packet class for entity teleports.
- **Entity**: The entity being teleported.

## Important Functions
- **TeleportEntityPacket(shared_ptr<Entity> e)**: Constructor that scales the entity's double coordinates by 32 into fixed-point integers.
- **read(DataInputStream *dis)**: Reads entity ID, coordinates, and rotation. Handles conditional `_LARGE_WORLDS` logic.
- **write(DataOutputStream *dos)**: Writes the teleport data.
- **isInvalidatedBy(shared_ptr<Packet> packet)**: Newer teleports for the same entity ID invalidate previous ones.

## Modding Notes
- Standard Minecraft uses fixed-point math (32.0 scale) for entity positions in packets. 4J's implementation also includes special handling for `_LARGE_WORLDS` using full integers.
- Categorized under **Movement**, **Entities**, and **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.world.entity.h`

---
**Related to:** [Movement](Movement.md), [Entities](Entities.md), [Networking](Networking.md)

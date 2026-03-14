# SetRidingPacket

## Purpose
The `SetRidingPacket` is used to synchronize the riding relationship between two entities. It informs the client which entity is acting as the rider and which is being ridden (mount).

## Key Classes
- **SetRidingPacket**: The main packet class handling the riding state.
- **Entity**: The base class for both the rider and the ridden entities.

## Important Functions
- **SetRidingPacket(shared_ptr<Entity> rider, shared_ptr<Entity> riding)**: Constructor that initializes the packet with the entity IDs of the rider and the mount.
- **read(DataInputStream *dis)**: Reads the rider and mount entity IDs from the network stream.
- **write(DataOutputStream *dos)**: Writes the rider and mount entity IDs to the network stream.
- **handle(PacketListener *listener)**: Dispatches the packet to the listener's `handleRidePacket` method.
- **isInvalidatedBy(shared_ptr<Packet> packet)**: Checks if a newer packet for the same rider should invalidate this one.

## Modding Notes
- This packet is essential for correctly displaying entities on mounts (like horses, pigs, or minecarts).
- A `riddenId` of `-1` indicates that the rider is dismounting.
- It is categorized under **Entities** and **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.world.entity.h`
- `PacketListener.h`

---
**Related to:** [Entities](Entities.md), [Networking](Networking.md)

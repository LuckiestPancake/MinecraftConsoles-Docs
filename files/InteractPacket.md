# InteractPacket

## Purpose
The `InteractPacket` communicates a player's interaction with another entity, whether it be a general interaction (like talking to a villager) or an attack.

## Key Classes
- `InteractPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the source entity ID, target entity ID, and the action byte.
- `write(DataOutputStream *dos)`: Writes the source entity ID, target entity ID, and the action byte.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleInteract` method.
- `getId()`: Returns the packet ID, which is 7.

## Modding Notes
- The `action` field distinguishes between `INTERACT` (0) and `ATTACK` (1).
- This packet is essential for all combat and NPC interaction mechanics.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Entities.

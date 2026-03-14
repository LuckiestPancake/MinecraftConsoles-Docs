# EntityEventPacket

## Purpose
The `EntityEventPacket` is used to send various status updates or events related to a specific entity, such as health changes, status effects, or other miscellaneous events.

## Key Classes
- `EntityEventPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the entity ID and the event ID byte.
- `write(DataOutputStream *dos)`: Writes the entity ID and the event ID byte.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleEntityEvent` method.
- `getId()`: Returns the packet ID, which is 38.

## Modding Notes
- Event IDs are often hardcoded and correspond to specific entity behaviors (e.g., tamed effects, death animations).
- It is a lightweight way to trigger client-side visual or behavioral responses for an entity.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Entities.

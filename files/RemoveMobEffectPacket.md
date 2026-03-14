# RemoveMobEffectPacket

## Purpose
The `RemoveMobEffectPacket` is used to inform a client that a specific status effect (e.g., Poison, Speed, Strength) should be removed from an entity.

## Key Classes
- `RemoveMobEffectPacket`: The main class representing the packet.
- `MobEffectInstance`: Represents the effect being removed.

## Important Functions
- `read(DataInputStream *dis)`: Reads the entity ID and the effect ID byte.
- `write(DataOutputStream *dos)`: Writes the entity ID and effect ID to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleRemoveMobEffect` method.
- `getId()`: Returns the packet ID, which is 42.

## Modding Notes
- Effect IDs are sent as single bytes.
- This packet is critical for correctly syncing the expiration or curing (e.g., by milk) of status effects in multiplayer.

## Important Dependencies
- `Packet.h`
- `MobEffectInstance.h`
- `PacketListener.h`

Cross-references: Entities.

# UpdateMobEffectPacket

## Purpose
The `UpdateMobEffectPacket` informs the client that an entity (player or mob) has been affected by a status effect (like Swiftness, Poison, or Strength).

## Key Classes
- **UpdateMobEffectPacket**: The packet class for effect updates.
- **MobEffectInstance**: Represents the active effect being synced.

## Important Functions
- **read(DataInputStream *dis)**: Reads entity ID, effect ID, amplifier, and duration.
- **write(DataOutputStream *dos)**: Writes the effect data.
- **isInvalidatedBy(shared_ptr<Packet> packet)**: Newer updates for the same effect on the same entity invalidate older ones.

## Modding Notes
- The `effectDurationTicks` is capped at `Short::MAX_VALUE`.
- If an effect's duration is greater than this limit, it is treated as "infinite" or "super long duration".
- Categorized under **Entities** and **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.world.effect.h`

---
**Related to:** [Entities](Entities.md), [Networking](Networking.md)

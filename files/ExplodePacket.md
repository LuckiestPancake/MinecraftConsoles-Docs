# ExplodePacket

## Purpose
The `ExplodePacket` notifies the client of an explosion event, including its location, radius, the blocks affected, and the resulting knockback on the player.

## Key Classes
- `ExplodePacket`: The main class representing the packet.
- `TilePos`: Represents the coordinates of blocks destroyed by the explosion.
- `Vec3`: Used for the knockback vector.

## Important Functions
- `read(DataInputStream *dis)`: Reads the explosion center, radius, a list of affected block positions (relative to the center), and knockback values.
- `write(DataOutputStream *dos)`: Writes the explosion data, optimizing the block positions as relative bytes.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleExplosion` method.
- `getId()`: Returns the packet ID, which is 60.

## Modding Notes
- The packet includes a `m_bKnockbackOnly` flag which, if true, skips the block destruction data and only applies knockback.
- Block positions are sent as offsets from the explosion center to save bandwidth.

## Important Dependencies
- `Packet.h`
- `TilePos.h`
- `Vec3.h`
- `PacketListener.h`

Cross-references: Entities, Movement.

# XZPacket

## Purpose
The `XZPacket` is a 4J-specific packet used to transmit a specific set of X and Z coordinates to the client for a given action.

## Key Classes
- **XZPacket**: The packet class for coordinate-based notifications.

## Important Functions
- **read(DataInputStream *dis)**: Reads a single-byte action ID and two integer coordinates (X and Z).
- **write(DataOutputStream *dos)**: Writes the action and coordinates.
- **handle(PacketListener *listener)**: Dispatches to `handleXZ`.

## Modding Notes
- The only defined action in the source is `STRONGHOLD (0)`, likely used to sync the location of a stronghold (e.g., when an Eye of Ender is used).
- Categorized under **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.world.item.h`

---
**Related to:** [Networking](Networking.md)

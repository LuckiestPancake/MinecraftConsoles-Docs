# SetTimePacket

## Purpose
The `SetTimePacket` synchronizes the world time with the client. It includes both the total game time (total ticks since world creation) and the day time (current time within the 24,000 tick cycle).

## Key Classes
- **SetTimePacket**: The main packet class for time synchronization.

## Important Functions
- **SetTimePacket(int64_t gameTime, int64_t dayTime, bool tickDayTime)**: Initializes the packet with world time data. Note: 4J implementation comments suggest daylight cycle rules are handled differently.
- **read(DataInputStream *dis)**: Reads two long (64-bit) values for game time and day time.
- **write(DataOutputStream *dos)**: Writes the time values to the stream.
- **isAync()**: Returns `true`, indicating this packet can be handled asynchronously.

## Modding Notes
- Setting `dayTime` to a negative value in some Minecraft versions indicates that the daylight cycle is frozen, though the 4J code has this commented out in favor of host options.
- Categorized under **Networking**.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

---
**Related to:** [Networking](Networking.md)

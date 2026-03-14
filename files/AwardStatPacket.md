# AwardStatPacket.h / AwardStatPacket.cpp

## Purpose
A network packet sent to clients to award a statistic or trigger an achievement/event.

## Key Classes
- `AwardStatPacket`: Inherits from `Packet`.

## Important Functions
- `handle()`: Dispatches the packet to the `PacketListener`.
- `read()` / `write()`: Handles serialization of the statistic ID and associated parameter data.
- `getCount()`: Returns the count/value of the stat being awarded (special handling for Durango/Xbox).
- `getParamData()`: Returns raw blob data, used for complex event parameters on certain platforms.

## Modding Notes
- Packet ID is 200.
- 4J Studios modified this to support "Durango" (Xbox One) platform-specific event blobs.
- Relates to **networking**.

## Important Dependencies
- `Packet.h`
- `DataInputStream.h`
- `DataOutputStream.h`
- `PacketListener.h`

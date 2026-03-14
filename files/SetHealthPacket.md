# SetHealthPacket

## Purpose
The `SetHealthPacket` is used to synchronize the player's health, hunger (food level), and saturation levels.

## Key Classes
- `SetHealthPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads health (float), food (short), saturation (float), and a damage source byte.
- `write(DataOutputStream *dos)`: Writes the health and food data to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleSetHealth` method.
- `getId()`: Returns the packet ID, which is 8.

## Modding Notes
- 4J Studios added the `damageSource` field (of type `ETelemetryChallenges`) to track the cause of health changes for telemetry purposes.
- This packet triggers the "red flash" or "shake" effect on the client's HUD when health decreases.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: UI.

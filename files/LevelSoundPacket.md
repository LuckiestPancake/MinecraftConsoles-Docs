# LevelSoundPacket

## Purpose
The `LevelSoundPacket` is used to play a sound effect at a specific location in the world with a defined volume and pitch.

## Key Classes
- `LevelSoundPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the sound ID, scaled X, Y, Z coordinates, volume, and pitch.
- `write(DataOutputStream *dos)`: Writes the sound parameters to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleSoundEvent` method.
- `getId()`: Returns the packet ID, which is 62.

## Modding Notes
- Coordinates are scaled by `LOCATION_ACCURACY` (8.0) to save bandwidth while maintaining precision.
- Pitch is sent as a float to maintain accuracy for musical elements like note blocks.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Networking.

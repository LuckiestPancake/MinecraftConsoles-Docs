# SetExperiencePacket

## Purpose
The `SetExperiencePacket` synchronizes the player's current experience levels and progress bar with the client for UI display.

## Key Classes
- `SetExperiencePacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads the experience progress (float), experience level (short), and total experience (short).
- `write(DataOutputStream *dos)`: Writes the experience values to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handleSetExperience` method.
- `getId()`: Returns the packet ID, which is 43.

## Modding Notes
- `experienceProgress` is a float between 0.0 and 1.0 representing the progress to the next level.
- This packet is exclusively used for the player receiving it.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: UI.

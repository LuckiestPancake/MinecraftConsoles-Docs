# PlayerInputPacket

## Purpose
The `PlayerInputPacket` is sent by the client to communicate raw movement inputs (strafe and forward/backward) and basic action states (jumping and sneaking) to the server.

## Key Classes
- `PlayerInputPacket`: The main class representing the packet.

## Important Functions
- `read(DataInputStream *dis)`: Reads strafe (`xxa`), forward (`yya`), `isJumping`, and `isSneaking`.
- `write(DataOutputStream *dos)`: Writes the input values to the stream.
- `handle(PacketListener *listener)`: Dispatches the packet to the listener's `handlePlayerInput` method.
- `getId()`: Returns the packet ID, which is 27.

## Modding Notes
- This packet provides the server with the player's intended movement direction, allowing the server to calculate the resulting motion while accounting for obstacles and physics.
- Both `xxa` and `yya` are floats, typically ranging from -1.0 to 1.0.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

Cross-references: Movement.

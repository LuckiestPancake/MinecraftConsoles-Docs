# UpdateGameRuleProgressPacket

## Purpose
The `UpdateGameRuleProgressPacket` is a 4J-specific packet used to notify the client about progress related to specific console game rules or challenges.

## Key Classes
- **UpdateGameRuleProgressPacket**: The packet class for progress updates.
- **ConsoleGameRules**: Defines the types of game rules and challenges.

## Important Functions
- **read(DataInputStream *dis)**: Reads the rule type, a message ID string, an icon ID, an auxiliary value, and a raw data payload.
- **write(DataOutputStream *dos)**: Writes the progress data.
- **handle(PacketListener *listener)**: Dispatches to `handleUpdateGameRuleProgressPacket`.

## Modding Notes
- This packet is used for console-specific features like achievement progress or "mini-game" state synchronization.
- It can carry up to 65536 bytes of arbitrary data.
- Categorized under **UI** and **Networking**.

## Important Dependencies
- `Packet.h`
- `ConsoleGameRules.h`

---
**Related to:** [UI](UI.md), [Networking](Networking.md)

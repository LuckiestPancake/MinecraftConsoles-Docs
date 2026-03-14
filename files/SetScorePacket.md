# SetScorePacket

## Purpose
The `SetScorePacket` is used to update or remove a score for a specific player (owner) within a scoreboard objective.

## Key Classes
- **SetScorePacket**: The main packet class for scoreboard score updates.
- **Score**: Represents the individual score being updated.
- **Scoreboard**: The overarching system managing objectives and scores.

## Important Functions
- **SetScorePacket(Score *score, int method)**: Constructor for updating or changing a score.
- **SetScorePacket(const wstring &owner)**: Constructor specifically for removing all scores for a player.
- **read(DataInputStream *dis)**: Reads the owner name, method (change/remove), objective name, and score value.
- **write(DataOutputStream *dos)**: Writes the scoreboard update data to the stream.
- **handle(PacketListener *listener)**: Dispatches to `handleSetScore`.

## Modding Notes
- `METHOD_CHANGE (0)` is used to set or update a score.
- `METHOD_REMOVE (1)` is used to delete a score entry.
- Max lengths for owner and objective names are enforced by `Player::MAX_NAME_LENGTH` and `Objective::MAX_NAME_LENGTH`.
- Categorized under **UI** and **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.world.scores.h`
- `net.minecraft.world.entity.player.h`

---
**Related to:** [UI](UI.md), [Networking](Networking.md)

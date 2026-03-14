# BedTile.h / BedTile.cpp

## Purpose
The block class for the Bed. It handles sleeping logic, respawn point setting, and multi-block structure management (head and foot pieces).

## Key Classes
- `BedTile`: Inherits from `DirectionalTile`.

## Important Functions
- `use()`: Triggered when a player right-clicks a bed. Handles sleeping, respawn point updates, and the "exploding in Nether/End" mechanic.
- `isHeadPiece()` / `isOccupied()`: Helper functions to parse block metadata.
- `findStandUpPosition()`: Determines a safe spot for the player to spawn after waking up.
- `neighborChanged()`: Ensures that if one half of the bed is broken, the other half is also removed.

## Modding Notes
- In 4J's implementation, beds in the Nether or End will explode, but they also check for `mayRespawn()` in the dimension.
- Includes console-specific messages like `IDS_TILE_BED_PLAYERSLEEP` for multiplayer.
- Relates to **blocks** and **entities** (players).

## Important Dependencies
- `DirectionalTile.h`
- `Player.h`
- `Level.h`
- `Biome.h`

# BlockDestructionProgress.h / BlockDestructionProgress.cpp

## Purpose
Tracks the progress of a block being broken by a player or entity. This data is used to render the "cracking" overlay on blocks.

## Key Classes
- `BlockDestructionProgress`: Simple data container for destruction state.

## Important Functions
- `setProgress()`: Sets the current breaking stage (0 to 10).
- `getUpdatedRenderTick()`: Used to determine when the destruction progress was last updated, helping the client clean up old overlays.

## Modding Notes
- Each destruction effect has a unique ID, allowing multiple blocks to be broken simultaneously (e.g., by different players).
- Relates to **rendering**.

## Important Dependencies
- None.

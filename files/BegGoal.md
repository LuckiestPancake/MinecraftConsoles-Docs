# BegGoal.h / BegGoal.cpp

## Purpose
An AI goal for wolves that causes them to look at a player holding a "bone" or food, tilting their head in interest.

## Key Classes
- `BegGoal`: Inherits from `Goal`.

## Important Functions
- `canUse()`: Checks if a player is nearby and holding an "interesting" item (bone for wild wolves, food for tame ones).
- `start()` / `stop()`: Toggles the `isInterested` state on the wolf.
- `tick()`: Forces the wolf to look at the player's head.
- `playerHoldingInteresting()`: Determines if the player's currently selected item triggers the begging behavior.

## Modding Notes
- 4J Studios added a `setLevel()` override for loading entities from schematics.
- Relates to **AI** and **entities** (Wolf).

## Important Dependencies
- `Goal.h`
- `Wolf.h`
- `Player.h`
- `Item.h`

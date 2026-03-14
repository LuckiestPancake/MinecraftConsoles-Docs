# BreakDoorGoal

## Purpose
Allows a mob (typically a Zombie) to interact with and eventually break down wooden doors.

## Key Classes
* `BreakDoorGoal`: The main class implementing the door-breaking behavior.
* `DoorInteractGoal`: The base class for door interactions.

## Important Functions
* `canUse()`: Determines if the mob is at a door it can break, checking for the `mobGriefing` game rule and if the door is closed.
* `tick()`: Handles the progression of breaking the door, playing wood-hitting sounds, and updating breaking progress in the level.
* `stop()`: Resets the breaking progress when the goal ends.

## Modding Notes
* The goal only functions if `RULE_MOBGRIEFING` is enabled.
* Doors are only fully destroyed if the level difficulty is set to `Difficulty::HARD`.
* Uses `LevelEvent::SOUND_ZOMBIE_WOODEN_DOOR` and `LevelEvent::SOUND_ZOMBIE_DOOR_CRASH`.

## Important Dependencies
* `DoorInteractGoal`
* `Mob`
* `Level`
* `GameRules`
* `SharedConstants`

## Category
Entities / AI

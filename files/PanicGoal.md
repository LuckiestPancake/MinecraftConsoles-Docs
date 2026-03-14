# PanicGoal

## Purpose
Causes passive or neutral mobs to flee in a random direction at high speed when they take damage or are set on fire.

## Key Classes
* `PanicGoal`: The AI goal for frantic escape.
* `PathfinderMob`: The mob performing the flee behavior.

## Important Functions
* `canUse()`: Checks if the mob was recently hurt or is currently on fire, and finds a random valid position to run towards.
* `start()`: Moves the mob towards the escape position using the specified `speedModifier`.

## Modding Notes
* Uses `RandomPos::getPos` to find a flight destination within a 5x4 range.
* Panic state persists for a random duration between 60 and 100 ticks.
* This goal typically takes high priority for passive mobs to ensure they react immediately to danger.

## Important Dependencies
* `PathfinderMob`
* `RandomPos`
* `Vec3`

## Category
Movement / AI

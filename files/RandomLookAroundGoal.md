# RandomLookAroundGoal

## Purpose
A simple idle behavior that causes a mob to occasionally rotate its head and look in a random direction.

## Key Classes
* `RandomLookAroundGoal`: The AI goal class for idle looking.
* `Mob`: The entity using the goal.

## Important Functions
* `canUse()`: Returns true based on a 2% random probability check.
* `start()`: Calculates a random horizontal direction and sets a random duration (20-40 ticks).
* `tick()`: Updates the mob's `LookControl` to face the randomly selected direction.

## Modding Notes
* This goal adds personality to idle mobs by making them appear to scan their surroundings.
* Requires both `MoveControlFlag` and `LookControlFlag` to ensure the mob doesn't move while looking around.

## Important Dependencies
* `Mob`
* `LookControl`

## Category
Entities / AI

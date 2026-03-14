# FollowParentGoal

## Purpose
Causes baby animals to stay close to their parents or other adult animals of the same species.

## Key Classes
* `FollowParentGoal`: The AI goal class for following parents.
* `Animal`: The mob type using this goal.

## Important Functions
* `canUse()`: Checks if the animal is a baby (age < 0) and searches for the nearest adult of the same type within range.
* `canContinueToUse()`: Continues until the baby reaches the adult or the adult moves too far away (16 blocks).
* `tick()`: Periodically recalculates the path to the parent.

## Modding Notes
* Uses `level->getEntitiesOfClass` with a specific bounding box growth (8, 4, 8) to find potential parents.
* The baby will stop following once it gets within 3 blocks of the parent.

## Important Dependencies
* `Animal`
* `Level`
* `PathNavigation`

## Category
Entities / AI / Movement

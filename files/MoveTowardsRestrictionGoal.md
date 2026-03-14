# MoveTowardsRestrictionGoal

## Purpose
Ensures that a mob stays within its allowed movement area by directing it back towards its restriction center if it wanders too far.

## Key Classes
* `MoveTowardsRestrictionGoal`: The AI goal class for maintaining boundaries.
* `PathfinderMob`: The mob being restricted.

## Important Functions
* `canUse()`: Triggers if `mob->isWithinRestriction()` returns false.
* `start()`: Calculates a random position towards the restriction center and moves the mob there.

## Modding Notes
* This goal is critical for mobs with "home" positions or those tethered to a specific area by world logic.
* Uses `RandomPos::getPosTowards` to find a valid pathable coordinate within 16 blocks of the restriction center.

## Important Dependencies
* `PathfinderMob`
* `RandomPos`
* `Vec3`

## Category
Movement / AI

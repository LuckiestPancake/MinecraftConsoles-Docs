# LeapAtTargetGoal

## Purpose
Causes a mob to perform a leaping attack towards its current target, providing a gap-closer for melee combat.

## Key Classes
* `LeapAtTargetGoal`: The AI goal class for leaping.
* `Mob`: The entity performing the leap.

## Important Functions
* `canUse()`: Triggers if the mob has a target, is on the ground, and is within a distance of 2 to 4 blocks.
* `start()`: Calculates the trajectory towards the target and applies velocity to the mob's `xd`, `yd`, and `zd`.

## Modding Notes
* This behavior is synonymous with the Spider's attack pattern.
* The leap height is configurable via the `yd` parameter in the constructor.
* Uses a 1-in-5 random chance in `canUse()` to prevent constant leaping.

## Important Dependencies
* `Mob`
* `LivingEntity`
* `Mth` (for distance and math)

## Category
Entities / AI / Movement

# RangedAttackGoal

## Purpose
A combat AI goal for mobs that attack from a distance (like Skeletons with bows or Snow Golems with snowballs).

## Key Classes
* `RangedAttackGoal`: The AI goal class for ranged combat.
* `RangedAttackMob`: An interface or base class that the mob must implement to perform the actual attack.
* `Mob`: The entity owning the goal.

## Important Functions
* `canUse()`: Checks for a valid attack target.
* `tick()`: Manages the distance to the target, ensuring the mob stays within `attackRadius`. It handles the attack cooldown and calls `performRangedAttack`.

## Modding Notes
* 4J added an explicit `Mob` parameter to the constructor to resolve type conversion ambiguities.
* The goal includes logic to "wind up" or wait before the first attack (`seeTime >= 20`).
* Attack power and timing are scaled based on the distance to the target relative to the max `attackRadius`.

## Important Dependencies
* `Mob`
* `RangedAttackMob`
* `LivingEntity`
* `Sensing`

## Category
Entities / AI / Combat

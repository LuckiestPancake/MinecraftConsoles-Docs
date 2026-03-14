# TargetGoal

## Purpose
An abstract base class for all AI goals that involve identifying, validating, and maintaining an attack target for a mob.

## Key Classes
* `TargetGoal`: The abstract base class.
* `PathfinderMob`: The entity type that uses targeting goals.
* `LivingEntity`: The potential target being evaluated.

## Important Functions
* `canAttack()`: Comprehensive check for target validity, including distance, line-of-sight, ally status, and invulnerability (e.g., Creative mode players).
* `canContinueToUse()`: Decides if the mob should keep its current target, handling "memory" of targets that have gone out of sight (default 60 ticks).
* `getFollowDistance()`: Returns the mob's `FOLLOW_RANGE` attribute, determining how far it will track a target.

## Modding Notes
* Implements a `reachCache` system to reduce the performance cost of pathfinding checks during target selection.
* Specifically prevents mobs from attacking their owners or other entities owned by the same person (via UUID check).
* `TargetFlag` (1) is the bitmask used for required control flags in targeting goals.

## Important Dependencies
* `PathfinderMob`
* `LivingEntity`
* `PathNavigation`
* `Sensing`
* `SharedMonsterAttributes`

## Category
Entities / AI

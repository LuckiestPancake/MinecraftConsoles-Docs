# MoveTowardsTargetGoal

## Purpose
Directs a mob to move towards its current attack target when the target is within a specific range, helping the mob close the distance for an engagement.

## Key Classes
* `MoveTowardsTargetGoal`: The AI goal class for approaching a target.
* `PathfinderMob`: The mob performing the movement.
* `LivingEntity`: The target being approached.

## Important Functions
* `canUse()`: Checks if the mob has a target and if that target is within the specified `within` distance.
* `start()`: Uses `RandomPos::getPosTowards` to calculate a path towards the target's coordinates.

## Modding Notes
* Unlike `MeleeAttackGoal`, this goal uses a random-position approach rather than direct pathfinding to the target's exact location, which can make movement feel more varied.
* The goal stops if the distance to the target exceeds the `within` threshold.

## Important Dependencies
* `PathfinderMob`
* `LivingEntity`
* `RandomPos`
* `Vec3`

## Category
Movement / AI

# NearestAttackableTargetGoal

## Purpose
A standard targeting goal used by many hostile mobs to find and lock onto the nearest valid attackable entity of a specific type.

## Key Classes
* `NearestAttackableTargetGoal`: The main targeting goal class.
* `TargetGoal`: The base class for targeting logic.
* `SubselectEntitySelector`: An internal helper to filter valid targets based on visibility and reachability.

## Important Functions
* `canUse()`: Periodically scans the area for entities of `targetType`. It sorts them by distance and selects the closest valid one.
* `start()`: Sets the mob's target to the identified entity.

## Modding Notes
* Uses an `EntitySelector` to perform complex filtering beyond just type checking.
* The search interval is randomized via `randomInterval` to distribute CPU load across multiple entities.
* Sorting is handled by the internal `DistComp` class, ensuring the closest target is always prioritized.

## Important Dependencies
* `PathfinderMob`
* `TargetGoal`
* `EntitySelector`
* `Level`

## Category
Entities / AI

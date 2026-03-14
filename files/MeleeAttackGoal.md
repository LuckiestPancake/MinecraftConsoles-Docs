# MeleeAttackGoal

## Purpose
A core combat AI goal that directs a mob to pathfind to its target and perform a melee attack when within range.

## Key Classes
* `MeleeAttackGoal`: The AI goal class for melee combat.
* `PathfinderMob`: The mob performing the attack.
* `LivingEntity`: The target of the attack.

## Important Functions
* `canUse()`: Checks if the mob has a valid, alive target and can create a path to it.
* `tick()`: Manages path updates, looks at the target, and triggers the attack logic (including swinging animation) when in range.
* `start()`/`stop()`: Manages the navigation lifecycle during combat.

## Modding Notes
* 4J added `setLevel()` for schematic support.
* Includes a path recalculation timer (4-10 ticks) to optimize performance.
* Attack range is calculated based on the mob's bounding box width (`(bbWidth * 2) * (bbWidth * 2) + target->bbWidth`).
* Supports an optional `attackType` filter to only target specific entity types.

## Important Dependencies
* `PathfinderMob`
* `LivingEntity`
* `PathNavigation`
* `Sensing`

## Category
Entities / AI / Movement

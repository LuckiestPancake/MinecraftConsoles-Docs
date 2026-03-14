# SwellGoal

## Purpose
The signature AI behavior for Creepers that manages their countdown to explosion when near a target.

## Key Classes
* `SwellGoal`: The AI goal class for creeper swelling.
* `Creeper`: The entity performing the action.

## Important Functions
* `canUse()`: Triggers if the creeper is already swelling or if a target is within 3 blocks.
* `tick()`: Checks distance and line-of-sight to the target. It sets `swellDir` to 1 (counting down) if the target is within 7 blocks and visible, otherwise it sets it to -1 (cooling down).

## Modding Notes
* The goal stops the creeper's navigation upon starting to ensure it stays in place while exploding.
* Relies on `creeper->getSensing()->canSee(target)` to prevent explosions through walls.

## Important Dependencies
* `Creeper`
* `Sensing`
* `LivingEntity`

## Category
Entities / AI / Combat

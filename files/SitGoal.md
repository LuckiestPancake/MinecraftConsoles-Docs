# SitGoal

## Purpose
Allows tamed animals (like Wolves or Cats) to stay in a stationary "sitting" position, effectively disabling their follow behavior.

## Key Classes
* `SitGoal`: The AI goal class for sitting.
* `TamableAnimal`: The tamed entity using the goal.

## Important Functions
* `canUse()`: Checks if the mob is tamed, on the ground, and the `_wantToSit` flag is set. It is overridden (returns false) if the owner is being attacked nearby.
* `start()`: Stops all current navigation and sets the mob's `sitting` state to true.
* `wantToSit()`: Toggles the goal's activation state, usually triggered by player interaction (right-clicking).

## Modding Notes
* While sitting, the mob's `JumpControlFlag` and `MoveControlFlag` are occupied, preventing other AI behaviors from moving the entity.
* The goal automatically prevents sitting if the mob is in water.

## Important Dependencies
* `TamableAnimal`
* `PathNavigation`
* `Control`

## Category
Entities / AI

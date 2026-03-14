# NonTameRandomTargetGoal

## Purpose
A specialized targeting goal for tamable animals (like Ocelots or Wolves) that causes them to target specific prey only while they are in a wild (non-tamed) state.

## Key Classes
* `NonTameRandomTargetGoal`: The specialized targeting goal.
* `NearestAttackableTargetGoal`: The base class providing the targeting logic.
* `TamableAnimal`: The entity using this goal.

## Important Functions
* `canUse()`: Extends the base targeting check with a condition that `tamableMob->isTame()` must be false.

## Modding Notes
* This ensures that tamed cats stop attacking chickens or tamed wolves stop attacking sheep automatically once they are tamed by a player.

## Important Dependencies
* `TamableAnimal`
* `NearestAttackableTargetGoal`

## Category
Entities / AI

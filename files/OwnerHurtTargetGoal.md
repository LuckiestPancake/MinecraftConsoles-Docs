# OwnerHurtTargetGoal

## Purpose
An offensive targeting goal for tamed animals that causes them to assist their owner by attacking whichever mob the owner is currently hitting.

## Key Classes
* `OwnerHurtTargetGoal`: The assistance-based targeting goal.
* `TamableAnimal`: The tamed entity assisting its owner.
* `LivingEntity`: Representing both the owner and the owner's target.

## Important Functions
* `canUse()`: Triggers if the mob is tamed and its owner has recently struck a valid target.
* `start()`: Locks the tamed animal's target to the entity the owner is attacking.

## Modding Notes
* Uses `owner->getLastHurtMob()` to identify what the owner is currently fighting.
* Like `OwnerHurtByTargetGoal`, it respects the `wantsToAttack` logic to avoid undesired combat.

## Important Dependencies
* `TamableAnimal`
* `LivingEntity`
* `TargetGoal`

## Category
Entities / AI

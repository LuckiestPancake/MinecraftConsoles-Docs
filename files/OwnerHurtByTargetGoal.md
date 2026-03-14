# OwnerHurtByTargetGoal

## Purpose
A defensive targeting goal for tamed animals (like Wolves) that triggers when their owner is attacked by another mob.

## Key Classes
* `OwnerHurtByTargetGoal`: The revenge-based targeting goal.
* `TamableAnimal`: The tamed entity defending its owner.
* `LivingEntity`: Representing both the owner and the attacker.

## Important Functions
* `canUse()`: Checks if the mob is tamed, its owner exists, and the owner was recently hurt by a valid attackable target.
* `start()`: Sets the tamed animal's target to the owner's attacker.

## Modding Notes
* Uses a timestamp system (`getLastHurtByMobTimestamp`) to ensure the animal only reacts to new attacks.
* Includes a call to `tameAnimal->wantsToAttack()` to respect specific targeting rules (e.g., wolves not attacking their owner's allies).

## Important Dependencies
* `TamableAnimal`
* `LivingEntity`
* `TargetGoal`

## Category
Entities / AI

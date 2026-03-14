# HurtByTargetGoal

## Purpose
A defensive targeting goal that causes a mob to retaliate against an attacker. It can also be configured to alert nearby mobs of the same type to assist in the fight.

## Key Classes
* `HurtByTargetGoal`: The AI goal class for "revenge" targeting.
* `TargetGoal`: The base class for targeting behaviors.
* `PathfinderMob`: The mob type using this goal.

## Important Functions
* `canUse()`: Checks if the mob has been hurt since the last time this goal ran and if the attacker is a valid target.
* `start()`: Sets the mob's target to the attacker. If `alertSameType` is true, it also notifies nearby similar mobs to target the same attacker.

## Modding Notes
* Implements pack behavior (e.g., Zombie pigmen or Wolves).
* Includes a check to ensure mobs don't target allies (`other->isAlliedTo(attacker)`).
* Uses the mob's `followDistance` attribute to determine the range for alerting others.

## Important Dependencies
* `PathfinderMob`
* `TargetGoal`
* `Level`
* `AABB`

## Category
Entities / AI

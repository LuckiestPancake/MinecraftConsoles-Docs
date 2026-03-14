# DefendVillageTargetGoal

## Purpose
An AI targeting goal for Iron Golems to identify and attack threats to their village.

## Key Classes
* `DefendVillageTargetGoal`: The targeting goal class.
* `VillagerGolem`: The owner of this goal.
* `Village`: The village context being defended.

## Important Functions
* `canUse()`: Checks the village for the closest aggressor attacking villagers or the golem itself.
* `start()`: Sets the Iron Golem's attack target to the identified threat.

## Modding Notes
* If no immediate aggressor is found, the goal occasionally checks for players with bad standing (low reputation) in the village.
* Heavily relies on the `Village` class's reputation and aggressor tracking systems.

## Important Dependencies
* `VillagerGolem`
* `Village`
* `TargetGoal`
* `LivingEntity`

## Category
Entities / AI

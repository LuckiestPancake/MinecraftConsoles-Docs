# MakeLoveGoal

## Purpose
The AI goal responsible for Villager breeding. It manages the courtship process and spawns a baby villager if the village population allows it.

## Key Classes
* `MakeLoveGoal`: The main AI goal class for villager breeding.
* `Villager`: The entity type involved in breeding.
* `Village`: Provides the context for population limits and breeding conditions.

## Important Functions
* `canUse()`: Checks if the villager is an adult, a nearby village exists, and the population is below the limit (35% of door count).
* `tick()`: Handles the approach to the partner and broadcasts love heart particles.
* `breed()`: Spawns a new baby villager and sets breeding cooldowns for the parents.

## Modding Notes
* 4J added `setLevel()` for schematic support and implemented a global limit on the number of villagers that can be bred (`level->canCreateMore`).
* Breeding requires both villagers to be in the "adult" state (age == 0).
* The goal uses `Village::isBreedTimerOk` to prevent rapid overpopulation.

## Important Dependencies
* `Villager`
* `Village`
* `Level`
* `EntityEvent`

## Category
Entities / AI

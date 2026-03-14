# BreedGoal

## Purpose
Handles the breeding logic for animals that are "in love," including finding a partner and spawning offspring.

## Key Classes
* `BreedGoal`: The class governing the breeding AI behavior.
* `Animal`: The base class for breedable mobs.
* `AgableMob`: Used for the resulting offspring.

## Important Functions
* `canUse()`: Checks if the animal is in love and if a suitable partner is nearby.
* `getFreePartner()`: Searches for a nearby animal of the same class that is also in love and can mate.
* `breed()`: Performs the actual breeding, spawning offspring, applying experience orbs, and handling stats/achievements.

## Modding Notes
* 4J added a specific fix for breeding not providing experience orbs (TU12).
* Offspring inherit age settings from `AgableMob::BABY_START_AGE`.
* Awards the `breedEntity` stat to the player who caused the love state.

## Important Dependencies
* `Animal`
* `Level`
* `ExperienceOrb`
* `GenericStats`
* `AgableMob`

## Category
Entities / AI

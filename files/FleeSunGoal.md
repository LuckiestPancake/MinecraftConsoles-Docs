# FleeSunGoal

## Purpose
Directs undead mobs (like Zombies or Skeletons) to find shade or shelter during the day to avoid taking fire damage from sunlight.

## Key Classes
* `FleeSunGoal`: The AI goal class for seeking shelter.
* `PathfinderMob`: The mob type using this goal.
* `Level`: Used to check sky visibility and time of day.

## Important Functions
* `canUse()`: Triggers if it is daytime, the mob is on fire, and can see the sky.
* `getHidePos()`: Searches for a nearby position that is not exposed to the sky.
* `start()`: Sets the mob's navigation to move towards the identified shelter.

## Modding Notes
* 4J added `setLevel()` for schematic loading support.
* The goal uses a random search (10 attempts) to find a suitable hiding spot within a 20x6x20 area.
* Relies on `level->canSeeSky()` to determine safe zones.

## Important Dependencies
* `PathfinderMob`
* `Level`
* `Vec3`
* `Mth`

## Category
Movement / AI

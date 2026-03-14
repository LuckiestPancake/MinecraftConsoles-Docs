# MoveThroughVillageGoal

## Purpose
Enables a mob to navigate through a village by moving between registered doors, often used by Raiders or wandering mobs.

## Key Classes
* `MoveThroughVillageGoal`: The AI goal class for village navigation.
* `Village`: The village being navigated.
* `DoorInfo`: The specific door locations used as waypoints.

## Important Functions
* `canUse()`: Identifies the next unvisited door in the village and creates a path to it.
* `getNextDoorInfo()`: Finds the closest door that hasn't been recently visited.
* `stop()`: Marks the current door as "visited" once the mob reaches it.

## Modding Notes
* Maintains a `visited` list of up to 15 doors to prevent the mob from looping between the same two houses.
* Pathfinding is performed with `canOpenDoors` set to false to ensure the mob moves *to* the door rather than trying to path through it immediately.
* Can be configured to only trigger at night via the `onlyAtNight` constructor parameter.

## Important Dependencies
* `PathfinderMob`
* `Village`
* `DoorInfo`
* `Path`

## Category
Movement / AI

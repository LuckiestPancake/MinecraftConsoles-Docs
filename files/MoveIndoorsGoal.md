# MoveIndoorsGoal

## Purpose
Directs a mob (typically a Villager) to seek indoor shelter when it starts raining or when night falls.

## Key Classes
* `MoveIndoorsGoal`: The AI goal class for seeking shelter.
* `Village`: Used to find nearby registered houses/doors.
* `DoorInfo`: Provides the "indoor" coordinates for a registered door.

## Important Functions
* `canUse()`: Triggers during rain or at night if a nearby village has a registered door.
* `start()`: Sets the mob's navigation to move towards the "indoor" side of the best available door.

## Modding Notes
* Uses `village->getBestDoorInfo()` to prioritize shelter locations.
* The goal is disabled if the mob's dimension has a ceiling (like the Nether).
* Implements a random 1-in-50 check in `canUse()` to stagger mob movement towards houses.

## Important Dependencies
* `PathfinderMob`
* `Village`
* `DoorInfo`
* `RandomPos`

## Category
Movement / AI

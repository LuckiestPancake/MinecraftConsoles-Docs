# RestrictOpenDoorGoal

## Purpose
An AI goal typically used by Villagers at night to ensure they stay behind closed doors and do not accidentally open them, protecting the village from invaders.

## Key Classes
* `RestrictOpenDoorGoal`: The AI goal class for door restriction.
* `Village`: Provides context for house and door locations.
* `DoorInfo`: Tracks the state and usage of specific doors.

## Important Functions
* `canUse()`: Triggers at night if the villager is very close to the "inside" of a registered village door.
* `start()`: Explicitly disables the mob's ability to open or pass through doors via its navigation settings.
* `tick()`: Increments the "booking count" on the `DoorInfo`, signaling that the door is currently "reserved" or in use by a resident.

## Modding Notes
* This goal is a key component of the Villager "staying safe at night" behavior.
* It stops once it is daytime or if the villager is no longer on the "inside" side of the door.

## Important Dependencies
* `PathfinderMob`
* `Village`
* `DoorInfo`
* `PathNavigation`

## Category
Entities / AI

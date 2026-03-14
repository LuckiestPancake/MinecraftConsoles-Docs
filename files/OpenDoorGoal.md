# OpenDoorGoal

## Purpose
An AI goal that allows intelligent mobs to open wooden doors to continue their pathfinding and optionally close them behind themselves.

## Key Classes
* `OpenDoorGoal`: The AI goal class for opening doors.
* `DoorInteractGoal`: The base class providing door detection logic.

## Important Functions
* `start()`: Sets the `DoorTile` to its open state in the world.
* `stop()`: If `closeDoor` is enabled, it sets the `DoorTile` back to its closed state.
* `tick()`: Decrements the interaction timer while the mob passes through.

## Modding Notes
* Extends `DoorInteractGoal` to inherit the logic for identifying doors along the mob's current path.
* Uses a `forgetTime` of 20 ticks to ensure the door stays open long enough for the mob to pass.

## Important Dependencies
* `Mob`
* `DoorTile`
* `DoorInteractGoal`
* `Level`

## Category
Entities / AI / Movement

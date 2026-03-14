# DoorInteractGoal

## Purpose
Base AI goal class for mobs that can interact with wooden doors, providing shared logic for door detection and navigation through doors.

## Key Classes
* `DoorInteractGoal`: The abstract base class for door-related goals.
* `DoorTile`: The block type being interacted with.
* `Mob`: The entity performing the interaction.

## Important Functions
* `canUse()`: Scans the mob's current path to find a door within range.
* `start()`: Initializes the interaction direction.
* `tick()`: Tracks the mob's position relative to the door to determine when it has passed through.

## Modding Notes
* This class is typically extended by `OpenDoorGoal` and `BreakDoorGoal`.
* Specifically checks for `Tile::door_wood_Id`.
* Integration with `PathNavigation` ensures the mob only interacts with doors it is allowed to open.

## Important Dependencies
* `Mob`
* `DoorTile`
* `PathNavigation`
* `Level`

## Category
Entities / AI / Movement

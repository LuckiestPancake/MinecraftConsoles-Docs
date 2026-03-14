# LookAtPlayerGoal

## Purpose
A social AI goal that causes a mob to turn its head towards a nearby player or another specific entity type.

## Key Classes
* `LookAtPlayerGoal`: The main AI goal class for looking behavior.
* `Mob`: The entity using the goal.

## Important Functions
* `canUse()`: Searches for a nearby entity of the specified type within a given radius.
* `tick()`: Updates the mob's `LookControl` to face the target's head position.
* `start()`: Determines a random duration for the gaze (40-80 ticks).

## Modding Notes
* Includes a probability check (default 2%) in `canUse()` to make the behavior feel more natural and less robotic.
* Supports looking at any entity class type specified via `type_info`.

## Important Dependencies
* `Mob`
* `Level`
* `LookControl`
* `Mth`

## Category
Entities / AI

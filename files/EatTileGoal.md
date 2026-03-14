# EatTileGoal

## Purpose
Allows a mob (such as a Sheep) to consume grass or tall grass blocks, typically used for restoring hunger or regrowing wool.

## Key Classes
* `EatTileGoal`: The AI goal class for eating tiles.
* `Mob`: The entity performing the action.
* `Level`: The world context where tiles are destroyed/modified.

## Important Functions
* `canUse()`: Checks if the mob is on a grass block or tall grass and applies a random chance for the goal to trigger.
* `start()`: Broadcasts the `EntityEvent::EAT_GRASS` to trigger animations on clients and stops the mob's navigation.
* `tick()`: Decrements the animation timer and, at the midpoint, replaces grass with dirt or removes tall grass, calling `mob->ate()`.

## Modding Notes
* 4J added `setLevel()` to support updating AI elements when loading entities from schematics.
* The eating chance is significantly higher for baby animals (1/50 vs 1/1000).
* The actual effect of eating (like regrowing wool) is handled in the mob's `ate()` implementation.

## Important Dependencies
* `Mob`
* `Level`
* `TallGrass`
* `Tile`
* `Mth` (Math utilities)

## Category
Entities / AI

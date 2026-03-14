# OcelotSitOnTileGoal

## Purpose
Enables tamed Ocelots (cats) to exhibit their signature behavior of seeking out and sitting on specific furniture-like blocks such as chests, beds, and lit furnaces.

## Key Classes
* `OcelotSitOnTileGoal`: The AI goal class for sitting on blocks.
* `Ocelot`: The tamed cat performing the behavior.

## Important Functions
* `canUse()`: Triggers randomly if the cat is tamed, not already sitting, and finds a valid target block nearby.
* `isValidTarget()`: Filters for `Tile::chest_Id` (if closed), `Tile::furnace_lit_Id`, or `Tile::bed_Id`.
* `tick()`: Manages the movement to the block and transitions the ocelot into its sitting state once it arrives.

## Modding Notes
* 4J added `setSittingOnTile()` to explicitly track this state.
* The search range for valid blocks is 8 blocks (`SEARCH_RANGE`).
* The cat will sit for a random duration between 60 and 180 seconds (`SIT_TICKS`).

## Important Dependencies
* `Ocelot`
* `Level`
* `ChestTileEntity`
* `BedTile`

## Category
Entities / AI / Movement

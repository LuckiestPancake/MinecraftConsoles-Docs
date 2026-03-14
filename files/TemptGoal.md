# TemptGoal

## Purpose
Causes passive or neutral mobs to follow a player who is holding a specific item, such as breeding food (wheat, carrots, etc.).

## Key Classes
* `TemptGoal`: The AI goal class for item-based attraction.
* `PathfinderMob`: The mob being tempted.
* `Player`: The player holding the tempting item.

## Important Functions
* `canUse()`: Checks for a player within 10 blocks holding the `itemId` specified in the constructor.
* `tick()`: Directs the mob to walk towards the player, stopping if it gets within 2.5 blocks to wait for the item to be used.
* `start()`/`stop()`: Manages water avoidance and "despawn protection" flags while the mob is being tempted.

## Modding Notes
* If `canScare` is enabled, the mob will stop following if the player rotates their head too quickly or moves abruptly.
* Calling `mob->setDespawnProtected()` ensures that animals following a player don't accidentally vanish due to world cleanup logic.
* A `calmDown` timer of 100 ticks is applied after the goal stops to prevent immediate re-triggering.

## Important Dependencies
* `PathfinderMob`
* `Player`
* `ItemInstance`
* `PathNavigation`

## Category
Entities / AI / Movement

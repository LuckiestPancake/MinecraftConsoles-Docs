# LookAtTradingPlayerGoal

## Purpose
Specialized version of `LookAtPlayerGoal` for Villagers that ensures they maintain eye contact with the player they are currently trading with.

## Key Classes
* `LookAtTradingPlayerGoal`: The specialized AI goal.
* `Villager`: The mob owning this goal.

## Important Functions
* `canUse()`: Specifically checks if `villager->isTrading()` is true and sets the `lookAt` target to the trading player.

## Modding Notes
* This goal has a fixed range of 8 blocks and specifically targets the `Player` class.
* Overrides the random probability check of the base class to ensure it always triggers during trading.

## Important Dependencies
* `Villager`
* `Player`
* `LookAtPlayerGoal`

## Category
Entities / AI

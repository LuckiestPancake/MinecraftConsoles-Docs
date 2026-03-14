# TradeWithPlayerGoal

## Purpose
A specialized AI goal for Villagers that locks their movement and keeps them stationary while a player has their trading interface open.

## Key Classes
* `TradeWithPlayerGoal`: The AI goal class for trading sessions.
* `Villager`: The mob being traded with.

## Important Functions
* `canUse()`: Checks if the villager has an active `tradingPlayer` within 4 blocks and if that player still has the trading menu open.
* `start()`: Immediately stops the villager's current navigation path.
* `stop()`: Resets the villager's `tradingPlayer` reference, allowing it to move freely again.

## Modding Notes
* This goal occupies both `JumpControlFlag` and `MoveControlFlag` to ensure the villager doesn't jump or walk away during a transaction.
* It will fail if the villager is hurt, in water, or not on the ground.

## Important Dependencies
* `Villager`
* `Player`
* `PathNavigation`
* `Control`

## Category
Entities / AI

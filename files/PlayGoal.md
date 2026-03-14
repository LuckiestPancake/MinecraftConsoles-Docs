# PlayGoal

## Purpose
An AI goal specifically for baby Villagers, allowing them to engage in "play" behavior by chasing each other or running to random locations within a village.

## Key Classes
* `PlayGoal`: The AI goal class for social play.
* `Villager`: The entity type (specifically babies) using this goal.

## Important Functions
* `canUse()`: Triggers for baby villagers (age < 0) with a 1-in-400 chance if another baby villager is nearby to play with.
* `start()`: Sets the villager into a "chasing" state.
* `tick()`: Directs the villager to move towards their "playmate" or a random nearby position if playing alone.

## Modding Notes
* Baby villagers are identified by having a negative age value.
* The goal uses `mob->setChasing(true)` to flag the entity for specific animations or particle effects associated with playing.
* Play sessions last for 1000 ticks (`playTime`).

## Important Dependencies
* `Villager`
* `Level`
* `RandomPos`
* `Vec3`

## Category
Entities / AI / Movement

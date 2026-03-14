# RunAroundLikeCrazyGoal

## Purpose
Governs the bucking and erratic movement behavior of a wild horse when a player attempts to tame it by riding it.

## Key Classes
* `RunAroundLikeCrazyGoal`: The AI goal class for horse taming.
* `EntityHorse`: The horse being tamed.
* `Player`: The player attempting the taming.

## Important Functions
* `canUse()`: Triggers if the horse is wild (not tamed) and has a rider.
* `tick()`: Periodically checks the horse's "temper" against a random threshold. If successful, the horse is tamed; otherwise, the rider is bucked off.

## Modding Notes
* Taming success is determined by `getRandom()->nextInt(maxTemper) < temper`.
* Failing to tame triggers `horse->makeMad()`, which typically involves a bucking animation and playing `EntityEvent::TAMING_FAILED`.
* Each bucking interval that doesn't result in taming or bucking off increases the horse's temper by 5.

## Important Dependencies
* `EntityHorse`
* `Player`
* `RandomPos`
* `Level`

## Category
Entities / AI / Movement

# RestrictSunGoal

## Purpose
A utility AI goal for undead mobs (like Zombies and Skeletons) that ensures they prefer shaded or indoor areas during the day to avoid taking sunlight damage.

## Key Classes
* `RestrictSunGoal`: The AI goal class for sun avoidance.
* `PathfinderMob`: The entity using the goal.

## Important Functions
* `canUse()`: Returns true if the current world time is day.
* `start()`: Enables the `setAvoidSun(true)` flag on the mob's navigation.
* `stop()`: Disables the `setAvoidSun` flag.

## Modding Notes
* This goal does not perform movement itself; it modifies the weight of paths calculated by `PathNavigation` to prioritize non-sunny tiles.
* Works in conjunction with `FleeSunGoal`.

## Important Dependencies
* `PathfinderMob`
* `PathNavigation`
* `Level`

## Category
Movement / AI

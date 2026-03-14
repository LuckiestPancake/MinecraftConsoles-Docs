# RandomStrollGoal

## Purpose
The primary idle movement goal for most mobs, causing them to wander aimlessly to random nearby positions.

## Key Classes
* `RandomStrollGoal`: The AI goal class for wandering.
* `PathfinderMob`: The mob type using this goal.

## Important Functions
* `canUse()`: Checks if the mob is ready to move (based on idle time) and finds a valid random destination using `RandomPos`.
* `start()`: Commences movement to the selected random coordinates.

## Modding Notes
* 4J modified this goal to support "extra wandering" (`isExtraWanderingEnabled`). This is used by the management system to force mobs to move across quadrant boundaries, assisting in despawning logic for animals not confined to fences.
* Normally triggers with a 1-in-120 chance if the mob has been idle for less than 5 seconds.

## Important Dependencies
* `PathfinderMob`
* `RandomPos`
* `Vec3`
* `SharedConstants`

## Category
Movement / AI

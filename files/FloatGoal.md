# FloatGoal

## Purpose
Ensures that mobs will swim/jump when in water or lava, preventing them from sinking and potentially drowning.

## Key Classes
* `FloatGoal`: The AI goal class for buoyancy.
* `Mob`: The entity using this goal.

## Important Functions
* `canUse()`: Returns true if the mob is currently in water or lava.
* `tick()`: Occasionally triggers a jump command to keep the mob at the surface.

## Modding Notes
* This goal is usually assigned the highest priority to ensure survival in fluids.
* Constructor explicitly calls `mob->getNavigation()->setCanFloat(true)`.

## Important Dependencies
* `Mob`
* `JumpControl`
* `PathNavigation`

## Category
Movement / AI

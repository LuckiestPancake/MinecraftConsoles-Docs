# OcelotAttackGoal

## Purpose
A specialized melee attack goal for Ocelots that incorporates unique movement styles like sneaking and sprinting based on the distance to the target.

## Key Classes
* `OcelotAttackGoal`: The AI goal class for ocelot combat.
* `Ocelot`: The entity type this goal is tailored for.

## Important Functions
* `canUse()`: Simple check if the ocelot has a valid attack target.
* `tick()`: Updates the ocelot's movement speed dynamically. It uses `SNEAK_SPEED_MOD` at distance, `SPRINT_SPEED_MOD` when closing in, and `WALK_SPEED_MOD` otherwise.

## Modding Notes
* 4J added `setLevel()` for schematic loading.
* The attack logic mimics the standard `MeleeAttackGoal` but with the added layer of speed modulation to represent a cat's hunting behavior.

## Important Dependencies
* `Mob`
* `Ocelot`
* `LivingEntity`
* `PathNavigation`

## Category
Entities / AI / Movement

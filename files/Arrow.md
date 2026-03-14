# Arrow

## Purpose
Represents the arrow entity in the world, including its movement, collision with blocks and entities, and damage calculation.

## Key Classes
- **Arrow**: Inherits from `Entity` and `Projectile`.

## Important Functions
- `shoot()`: Sets the initial velocity and direction of the arrow.
- `tick()`: Handles the arrow's flight logic, gravity, and collision detection.
- `playerTouch()`: Handles a player picking up the arrow if allowed.
- `setBaseDamage()`/`getBaseDamage()`: Manages the damage dealt by the arrow.

## Modding Notes
Supports different pickup states (`PICKUP_ALLOWED`, `PICKUP_DISALLOWED`, `PICKUP_CREATIVE_ONLY`). 4J Studios added common initialization code in `_init()`.

## Important Dependencies
- `Entity.h`
- `Projectile.h`

[Category: Entities]

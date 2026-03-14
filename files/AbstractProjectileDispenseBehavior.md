# AbstractProjectileDispenseBehavior

## Purpose
Defines the base behavior for dispensers when firing projectiles. It handles the common logic of spawning the projectile, setting its velocity, and consuming the item.

## Key Classes
- **AbstractProjectileDispenseBehavior**: Inherits from `DefaultDispenseItemBehavior` to provide projectile-specific dispensing logic.

## Important Functions
- `execute()`: Main logic that spawns the projectile using `getProjectile()` and launches it.
- `getProjectile()`: Pure virtual function that must be implemented by subclasses to specify which projectile entity to spawn.
- `playSound()`: Plays the launch sound.
- `getPower()`: Determines the initial velocity of the projectile.

## Modding Notes
Subclasses like those for arrows or snowballs implement `getProjectile()` to return the appropriate entity type.

## Important Dependencies
- `DefaultDispenseItemBehavior.h`
- `Projectile.h`
- `DispenserTile.h`

[Category: Entities]

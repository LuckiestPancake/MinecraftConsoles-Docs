# `AbstractProjectileDispenseBehavior.cpp`

## Purpose
This file implements the `AbstractProjectileDispenseBehavior` class, which defines the core logic for how dispensers behave when dispensing items that are projectiles (like arrows, snowballs, or fire charges). It handles spawning the projectile entity, setting its initial velocity and trajectory, playing a sound, and consuming the dispensed item.

## Key Classes
- **`AbstractProjectileDispenseBehavior`**: The abstract base class that handles the common logic for dispensing projectiles. It inherits from `DefaultDispenseItemBehavior` implicitly through its usage pattern.
- **`ItemInstance`**: Represents the stack of items being dispensed.
- **`BlockSource`**: Provides context about the dispenser's location and world.
- **`Level`**: Represents the game world where the projectile will be spawned.
- **`Position`**: Represents the 3D coordinates where the projectile is spawned.
- **`FacingEnum`**: Used to determine the direction the dispenser is facing, which dictates the projectile's initial trajectory.
- **`Projectile`**: The abstract base class for all projectile entities.
- **`DispenserTile`**: The tile entity representing the dispenser block.

## Important Functions
- **`execute(BlockSource *source, shared_ptr<ItemInstance> dispensed)`**: The main function called when the dispenser dispenses an item. It calls `getProjectile()` to create the specific projectile, then `shoot()` to give it velocity based on the dispenser's facing direction, adds it to the world, and removes one item from the dispensed stack.
- **`getProjectile(Level *world, Position pos)`**: A pure virtual function (intended to be overridden by subclasses) that must return the specific `Projectile` entity to be spawned (e.g., an `Arrow` or `Snowball`).
- **`playSound(BlockSource *source)`**: Plays a generic "launch" sound effect associated with dispensing a projectile.
- **`getUncertainty()`**: Returns a float value representing the randomness or spread applied to the projectile's trajectory.
- **`getPower()`**: Returns a float value representing the initial velocity or "power" of the projectile.

## Modding Notes
- Subclasses of `AbstractProjectileDispenseBehavior` would implement `getProjectile()` to define custom projectile types.
- The `getPower()` and `getUncertainty()` methods can be overridden to modify projectile behavior.
- The `playSound()` method can be customized for specific projectile launch sounds.

## Important Dependencies
- `..\Minecraft.World
et.minecraft.core.h` (likely for `Position`, `FacingEnum`)
- `..\Minecraft.World
et.minecraft.world.entity.projectile.h` (for `Projectile` and its subclasses)
- `..\Minecraft.World
et.minecraft.world.level.tile.h` (for `DispenserTile`, `BlockSource`)
- `..\Minecraft.World
et.minecraft.world.level.h` (for `Level`)

## Category
- Entities (Projectiles)
- World Interaction
- Dispenser Logic

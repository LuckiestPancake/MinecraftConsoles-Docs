# `AbstractProjectileDispenseBehavior.h`

## Purpose
This header file declares the `AbstractProjectileDispenseBehavior` class, which defines the abstract interface for dispensing projectile items from dispensers. It provides a base class for specific projectile types (like arrows or fireballs) to inherit from, enforcing common behavior such as spawning the projectile, setting its trajectory, and playing a sound.

## Key Classes
- **`AbstractProjectileDispenseBehavior`**: The abstract base class that defines the interface for projectile dispensing. It inherits from `DefaultDispenseItemBehavior`.
- **`DefaultDispenseItemBehavior`**: The base class for all dispenser item behaviors.
- **`ItemInstance`**: Represents the stack of items being dispensed.
- **`BlockSource`**: Provides the context (location, world, block data) of the dispenser.
- **`Position`**: Represents the 3D coordinates for spawning the projectile.
- **`Projectile`**: The abstract base class for projectile entities.

## Important Functions
- **`execute(BlockSource *source, shared_ptr<ItemInstance> dispensed)`**: The main function that orchestrates the dispensing process. It calls other protected/virtual functions to create, launch, and add the projectile to the world.
- **`playSound(BlockSource *source)`**: A protected virtual function to play a sound when the projectile is launched. Derived classes can override this for custom sounds.
- **`getProjectile(Level *world, Position *position)`**: A pure virtual function that derived classes *must* implement to specify which `Projectile` entity to create and return.
- **`getUncertainty()`**: Returns a float representing the randomness applied to the projectile's trajectory.
- **`getPower()`**: Returns a float representing the initial velocity of the projectile.

## Modding Notes
- This class is abstract, requiring derived classes to implement `getProjectile`.
- Subclasses can override `playSound`, `getPower`, and `getUncertainty` to customize projectile behavior.

## Important Dependencies
- **`..\Minecraft.World\DefaultDispenseItemBehavior.h`**: Base class for dispenser behaviors.
- **`..\Minecraft.World
et.minecraft.core.h`**: Likely provides `Position` and other core types.
- **`..\Minecraft.World
et.minecraft.world.entity.projectile.h`**: For the `Projectile` class.
- **`..\Minecraft.World
et.minecraft.world.level.tile.h`**: For `BlockSource` and `DispenserTile`.
- **`..\Minecraft.World
et.minecraft.world.level.h`**: For `Level` context.

## Category
- Entities (Projectiles)
- Dispenser Logic
- World Interaction

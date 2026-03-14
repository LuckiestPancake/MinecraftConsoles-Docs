# Blaze

## Purpose
The `Blaze` class represents the Blaze mob, a fiery, flying hostile creature found in the Nether. Blazes are known for their ability to shoot fireballs and their resistance to fire.

## Key Classes
- `Monster`: The base class for hostile creatures.
- `Entity`: The base class for all game entities.
- `Level`: Represents the game world.
- `DamageSource`: Represents the source of damage.
- `CompoundTag`: For saving and loading entity data.
- `SharedMonsterAttributes`: For defining entity attributes like attack damage.
- `SmallFireball`: The projectile entity fired by the Blaze.

## Important Functions
- `Blaze(Level *level)`: Constructor for the Blaze. Initializes its attributes, sets it on fire, and sets up its AI.
- `registerAttributes()`: Sets the base attack damage for the Blaze.
- `defineSynchedData()`: Initializes synched data, specifically a flag (`DATA_FLAGS_ID`) to track if the Blaze is "charged" (preparing to fire).
- `getAmbientSound()`, `getHurtSound()`, `getDeathSound()`: Returns the sound IDs for the Blaze's various actions.
- `getLightColor()`: Returns a full bright light value, indicating the Blaze emits light.
- `getBrightness()`: Returns 1.0f, indicating it's fully bright.
- `aiStep()`: The main AI loop for the Blaze. It handles flying behavior, seeking targets, and firing projectiles. It also handles extinguishing itself in water/rain and adding particle effects.
- `checkHurtTarget(shared_ptr<Entity> target, float d)`: Handles the Blaze's attack logic, including deciding when to fire fireballs and managing the charging state.
- `causeFallDamage(float distance)`: Overridden to do nothing, as Blazes don't take fall damage.
- `getDeathLoot()`: Returns the item ID for Blaze Rods.
- `isOnFire()`: Returns true if the Blaze is "charged", making it appear on fire.
- `dropDeathLoot(...)`: Spawns Blaze Rods and Glowstone Dust upon death, with chances influenced by the killer and enchantment levels.
- `isCharged()`: Checks the charged state from synched data.
- `setCharged(bool value)`: Sets the charged state in synched data.
- `isDarkEnoughToSpawn()`: Always returns true, as Blazes can spawn in any light level in the Nether.

## Modding Notes
- The `DATA_FLAGS_ID` is used for the `isCharged()` state. This could potentially be extended for other states.
- The `aiStep()` and `checkHurtTarget()` functions contain the core logic for the Blaze's movement (flying with height offset) and ranged attack. Modifying these can alter its combat behavior.
- The `dropDeathLoot()` function determines what items are dropped. This can be modified to change loot tables.
- The Blaze is immune to fire damage, which is set in the constructor.

## Important Dependencies
- `Monster.h`: Inherits from `Monster` for hostile mob behavior.
- `DamageSource.h`: For handling damage taken.
- `Level.h`: For world interactions and spawning entities.
- `SharedConstants.h`: For constants like `TICKS_PER_SECOND` and `FULLBRIGHT_LIGHTVALUE`.
- `net.minecraft.world.entity.projectile.SmallFireball.h`: For the projectile fired by the Blaze.
- `SoundTypes.h`: For sound constants.

**Cross-references:**
- AI/Behavior: `aiStep()`, `checkHurtTarget()`, `isCharged()`, `setCharged()`, `Monster`
- Combat: `registerAttributes()`, `getDeathLoot()`, `dropDeathLoot()`
- Entities: `Monster`, `Entity`, `SmallFireball`
- World Interaction: `isOnFire()`, `getLightColor()`, `level->playSound()`, `level->addEntity()`
- Data Handling: `defineSynchedData()`
- Sounds: `getAmbientSound()`, `getHurtSound()`, `getDeathSound()`

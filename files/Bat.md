# Bat

## Purpose
The `Bat` class represents the bat mob in the game. Bats are passive, flying creatures that primarily inhabit caves and dark areas. They have a unique AI that allows them to fly and rest on ceilings.

## Key Classes
- `AmbientCreature`: The base class for passive, non-hostile mobs that emit ambient sounds.
- `Entity`: The base class for all game entities.
- `Level`: Represents the game world.
- `Pos`: A structure used to store 3D coordinates.
- `CompoundTag`: Used for reading and writing entity data to save files.
- `DamageSource`: Represents the source of damage taken by an entity.

## Important Functions
- `Bat(Level *level)`: Constructor for the Bat entity.
- `defineSynchedData()`: Initializes the synchronized data for the bat, including its resting state flag.
- `isResting()`: Checks if the bat is currently resting.
- `setResting(bool value)`: Sets the resting state of the bat.
- `getAmbientSound()`, `getHurtSound()`, `getDeathSound()`: Returns the sound IDs associated with the bat's actions.
- `tick()`: Updates the bat's state each game tick, handling movement and resting.
- `newServerAiStep()`: Implements the bat's AI logic on the server side, including finding roosting spots and flying to target positions.
- `hurt(DamageSource *source, float dmg)`: Handles damage taken by the bat, including interrupting its resting state.
- `readAdditionalSaveData(CompoundTag *tag)`: Loads additional data for the bat from save files.
- `addAdditonalSaveData(CompoundTag *entityTag)`: Saves additional data for the bat to save files.
- `canSpawn()`: Determines if a bat can spawn at its current location, considering light levels and biome.

## Modding Notes
- The `DATA_ID_FLAGS` synched data is used to store the `FLAG_RESTING` state. Modders could potentially use this for other states if expanded.
- The AI logic in `newServerAiStep` defines the bat's flight and roosting behavior. Modifications here could alter how bats navigate or interact with the environment.
- Custom sounds could be introduced by modifying the sound ID return values in `getAmbientSound`, `getHurtSound`, and `getDeathSound`.

## Important Dependencies
- `AmbientCreature.h`: For inheriting ambient creature properties.
- `Level.h`: For world interaction, like checking light levels and finding players.
- `net.minecraft.world.phys.Pos.h`: For handling target positions.
- `CompoundTag.h`: For saving and loading entity data.
- `DamageSource.h`: For handling damage.
- `SharedMonsterAttributes.h`: For defining entity attributes like health.
- `Sound`: For playing sounds.

**Cross-references:**
- Movement: `tick()`, `newServerAiStep()`, `Pos`
- Entities: `AmbientCreature`, `Entity`
- AI/Behavior: `newServerAiStep()`, `isResting()`, `setResting()`, `doPush()`, `pushEntities()`
- World Interaction: `canSpawn()`, `level->isSolidBlockingTile()`
- Data Handling: `defineSynchedData()`, `readAdditionalSaveData()`, `addAdditonalSaveData()`
- Sounds: `getAmbientSound()`, `getHurtSound()`, `getDeathSound()`

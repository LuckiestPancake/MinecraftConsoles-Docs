# BaseMobSpawner.h / BaseMobSpawner.cpp

## Purpose
Contains the core logic for mob spawner blocks and minecart spawners, handling spawn delays, entity selection, and the spawning process.

## Key Classes
- `BaseMobSpawner`: The main logic class for mob spawning.
- `BaseMobSpawner::SpawnData`: Nested class representing a potential entity type and its NBT data for spawning.

## Important Functions
- `tick()`: The main update loop; handles particle effects and counts down the spawn delay.
- `loadDataAndAddEntity()`: Prepares the entity (loading NBT, setting up riders) and adds it to the world.
- `delay()`: Resets the spawn delay to a random value between `minSpawnDelay` and `maxSpawnDelay`.
- `load()` / `save()`: Handles serialization of spawner settings (entity ID, range, count, potentials).
- `getDisplayEntity()`: Returns the entity used for the spinning preview inside the spawner.

## Modding Notes
- Supports complex spawning scenarios, including "SpawnPotentials" for randomizing what a single spawner produces.
- Relates to **entities**.

## Important Dependencies
- `WeighedRandom.h`
- `EntityIO.h`
- `Level.h`
- `CompoundTag.h`

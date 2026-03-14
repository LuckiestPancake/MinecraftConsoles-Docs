# Abilities

## Purpose
The Abilities class manages a player's special capabilities, such as invulnerability, flying, and building permissions. It is responsible for tracking these states and persisting them to NBT data.

## Key Classes
- **Abilities**: The class holding the player's ability flags and speeds.

## Important Functions
- `addSaveData()`: Saves the current abilities to a CompoundTag (NBT).
- `loadSaveData()`: Loads abilities from a CompoundTag (NBT).
- `getFlyingSpeed()`, `setFlyingSpeed()`: Accessors for the player's flight speed.
- `getWalkingSpeed()`, `setWalkingSpeed()`: Accessors for the player's walking speed.

## Modding Notes
Includes a `debugflying` flag when `_DEBUG_MENUS_ENABLED` is defined, which can be useful for development and testing.

## Important Dependencies
- `CompoundTag.h`

[Category: Entities]

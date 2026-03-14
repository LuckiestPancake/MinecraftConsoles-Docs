# BeaconTileEntity.h / BeaconTileEntity.cpp

## Purpose
Manages the state and logic of a Beacon block, including pyramid detection, power application, and inventory.

## Key Classes
- `BeaconTileEntity`: Inherits from `TileEntity` and implements `Container`.

## Important Functions
- `tick()`: Periodically checks the pyramid structure and applies effects to nearby players.
- `updateShape()`: Checks for a valid pyramid (Emerald, Gold, Diamond, or Iron blocks) below the beacon and a clear view of the sky above.
- `applyEffects()`: Grants the selected primary and secondary `MobEffect` to players within range based on pyramid size.
- `load()` / `save()`: Serializes the beacon's powers and pyramid level.

## Modding Notes
- `BEACON_EFFECTS` is a static 2D array defining which effects are available at each pyramid tier.
- 4J Studios added a `clone()` method for TileEntities.
- Relates to **entities** and **redstone** (as it provides a signal/effect).

## Important Dependencies
- `TileEntity.h`
- `Container.h`
- `MobEffect.h`
- `AABB.h`

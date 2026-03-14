# BasePressurePlateTile.h / BasePressurePlateTile.cpp

## Purpose
Abstract base class for pressure plate blocks (stone, wood, and weighted). It handles shape updates, collision detection for triggering, and redstone signal logic.

## Key Classes
- `BasePressurePlateTile`: Inherits from `Tile`.

## Important Functions
- `updateShape()`: Adjusts the block's bounding box based on whether it is currently pressed.
- `checkPressed()`: Compares the current signal strength with the previous state and updates the block/neighbors if it changed.
- `entityInside()`: Triggered when an entity overlaps the block; checks if the plate should be pressed.
- `getSignalStrength()`: Pure virtual function to determine how much signal should be generated (e.g., based on entity count or type).

## Modding Notes
- Subclasses must implement `getSignalStrength`, `getSignalForData`, and `getDataForSignal`.
- Relates to **entities** (for triggering) and **redstone**.

## Important Dependencies
- `Tile.h`
- `AABB.h`
- `Level.h`

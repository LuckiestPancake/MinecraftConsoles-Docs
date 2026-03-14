# BaseRailTile.h / BaseRailTile.cpp

## Purpose
Base class for all rail blocks (normal, powered, detector, activator). It contains the complex logic for rail connections, curves, and slopes.

## Key Classes
- `BaseRailTile`: Inherits from `Tile`.
- `BaseRailTile::Rail`: Internal helper class that manages the connections and state of a single rail block.

## Important Functions
- `isRail()`: Static helper to check if a block ID corresponds to any rail type.
- `updateDir()`: Triggers the connection logic for a rail at a specific position.
- `BaseRailTile::Rail::place()`: Determines the correct orientation (direction) of the rail based on neighboring rails.
- `BaseRailTile::Rail::connectTo()`: Establishes a connection between two rail blocks.

## Modding Notes
- The connection logic is one of the most complex parts of block behavior in Minecraft, handling slopes (DIR 2-5) and curves (DIR 6-9).
- 4J Studios added safety checks to prevent crashes if a rail's ID changes unexpectedly during processing.
- Relates to **movement** (minecarts) and **redstone** (for powered rails).

## Important Dependencies
- `Tile.h`
- `TilePos.h`
- `Level.h`

# BasicTree.h / BasicTree.cpp

## Purpose
A base class for complex, branching tree features in the world. It uses an algorithm to generate a trunk, branches, and foliage clusters based on several scaling factors.

## Key Classes
- `BasicTree`: Inherits from `Feature`.

## Important Functions
- `place()`: The entry point for generating a tree at a specific location.
- `prepare()`: Calculates the positions for all foliage clusters and branches before placing blocks.
- `limb()`: Draws a line of log blocks between two points, handling the orientation (facing) of the logs.
- `foliageCluster()`: Generates a sphere-like cluster of leaf blocks.
- `checkLocation()`: Verifies that the tree has enough space and is resting on valid ground (grass/dirt).

## Modding Notes
- Uses a `trunkHeightScale` (default 0.618, the Golden Ratio) to determine where branches start.
- 4J Studios added a check to prevent trees from overlapping with "game rule structures" during generation.
- Relates to **world generation**.

## Important Dependencies
- `Feature.h`
- `Level.h`
- `Mth.h`
- `Tile.h`

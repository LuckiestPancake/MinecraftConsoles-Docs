# BirchFeature.h / BirchFeature.cpp

## Purpose
A world generation feature that places a Birch tree.

## Key Classes
- `BirchFeature`: Inherits from `Feature`.

## Important Functions
- `place()`: Attempts to place a Birch tree. It checks for space, valid ground (grass/dirt), and then places the white-stained logs and birch leaves.

## Modding Notes
- Includes 4J's "game rule structure" intersection check to prevent trees from growing through generated structures.
- Tree height is randomized between 5 and 7 blocks.
- Relates to **world generation**.

## Important Dependencies
- `Feature.h`
- `Level.h`
- `Tile.h`
- `LeafTile.h`
- `TreeTile.h`

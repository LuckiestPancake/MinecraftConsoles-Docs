# AddMushroomIslandLayer

## Purpose
A world generation layer specifically for spawning Mushroom Island biomes. It looks for land surrounded by ocean and has a small chance to convert it into a Mushroom Island.

## Key Classes
- **AddMushroomIslandLayer**: Inherits from `Layer`.

## Important Functions
- `getArea()`: Scans the map and applies a 1/100 chance to spawn a Mushroom Island biome in appropriate locations.

## Modding Notes
Part of the biome generation pipeline, usually applied after basic land/ocean distribution.

## Important Dependencies
- `Layer.h`
- `Biome.h`

[Category: Rendering]

# BiomeInitLayer.h / BiomeInitLayer.cpp

## Purpose
A world generation layer responsible for initializing the primary biomes (Desert, Forest, Extreme Hills, Swampland, Plains, Taiga, and Jungle) from the initial "land" map.

## Key Classes
- `BiomeInitLayer`: Inherits from `Layer`.

## Important Functions
- `getArea()`: Processes a region of the world map. It takes the output from the parent layer and replaces generic "land" values with specific biome IDs based on the `LevelType`.

## Modding Notes
- Supports legacy generation (Normal 1.1) which has a different set of starting biomes.
- 4J Studios added Jungle to the modern (Normal) generation.
- Relates to **world generation**.

## Important Dependencies
- `Layer.h`
- `Biome.h`
- `LevelType.h`
- `IntCache.h`

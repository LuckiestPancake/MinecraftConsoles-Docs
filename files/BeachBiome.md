# BeachBiome.h / BeachBiome.cpp

## Purpose
Defines the properties for the Beach biome, characterized by sand top/filler materials and a lack of trees.

## Key Classes
- `BeachBiome`: Inherits from `Biome`.

## Important Functions
- `BeachBiome()`: Constructor that sets up the materials (sand), clears default friendly mob spawns, and configures the decorator (no trees, cacti, or reeds).

## Modding Notes
- 4J Studios added `friendlies_chicken` to the clear list, indicating a console-specific adjustment to mob spawning.
- Relates to **world generation**.

## Important Dependencies
- `Biome.h`
- `Tile.h`
- `BiomeDecorator.h`

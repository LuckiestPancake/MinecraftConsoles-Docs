# BiomeSource.h / BiomeSource.cpp

## Purpose
The primary interface for retrieving biome information at any given coordinate in the world. It manages the layer-based generation system and provides caching for performance.

## Key Classes
- `BiomeSource`: The main class for accessing biomes, temperatures, and downfall values.

## Important Functions
- `getBiome()`: Returns the `Biome` at a specific X, Z coordinate (using the cache).
- `getBiomeBlock()`: Fills a `BiomeArray` with biome data for a specified region.
- `findSeed()`: 4J Studios added this function to "brute-force" search for a world seed that matches specific criteria (e.g., has all "critical" biomes and not too much ocean).
- `getIsMatch()`: Internal helper used by `findSeed` to validate if a seed meets the desired biome distribution.

## Modding Notes
- 4J Studios significantly modified this to support console-specific features like "Find Seed" and fixed-size worlds.
- Includes platform-specific optimizations for PS Vita and Durango (Xbox One).
- Relates to **world generation**.

## Important Dependencies
- `Biome.h`
- `Layer.h`
- `BiomeCache.h`
- `LevelType.h`

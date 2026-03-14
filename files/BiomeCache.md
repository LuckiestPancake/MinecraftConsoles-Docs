# BiomeCache.h / BiomeCache.cpp

## Purpose
Caches biome data for world regions to improve performance during world generation and rendering. Instead of recalculating biome data for every block, it stores it in "Blocks" (16x16 areas).

## Key Classes
- `BiomeCache`: Manages the cache.
- `BiomeCache::Block`: Represents a cached 16x16 area of biome indices.

## Important Functions
- `getBlockAt()`: Retrieves or creates a cached block for a given world coordinate.
- `getBiome()` / `getTemperature()` / `getDownfall()`: Convenience methods to get data from the cache.
- `update()`: Periodic cleanup that removes old, unused blocks from the cache to save memory.

## Modding Notes
- 4J Studios optimized the `Block` class to store only `biomeIndices` (bytes) instead of full biome objects or floats, significantly reducing memory usage.
- Uses `CRITICAL_SECTION` for thread safety, as biome lookups can happen during multi-threaded world generation or rendering.
- Relates to **world generation** and **rendering**.

## Important Dependencies
- `BiomeSource.h`
- `Biome.h`
- `JavaIntHash.h`

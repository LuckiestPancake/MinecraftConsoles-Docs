# BiomeDecorator.h / BiomeDecorator.cpp

## Purpose
Handles the "decoration" phase of world generation for a specific biome. It places features like ores, flowers, trees, and small structures (like desert wells or mushrooms) in a 16x16 chunk area.

## Key Classes
- `BiomeDecorator`: The main coordinator for biome-specific feature placement.

## Important Functions
- `decorate()`: Orchestrates the entire decoration process, calling specialized methods for ores, sand/clay, and biological features.
- `decorateOres()`: Places dirt, gravel, coal, iron, gold, redstone, diamond, and lapis ores.
- `decorateDepthSpan()`: Helper to place a feature a certain number of times within a specific Y-range.
- `_init()`: Initializes the static `Feature` instances used across all decoration passes.

## Modding Notes
- Each `Biome` has its own `BiomeDecorator` instance (or a subclass) with different settings for `treeCount`, `flowerCount`, etc.
- 4J Studios added `PIX` events for profiling the performance of different decoration stages.
- Relates to **world generation**.

## Important Dependencies
- `Biome.h`
- `Level.h`
- `Feature.h`
- `Random.h`
- `OreFeature.h`
- `FlowerFeature.h`

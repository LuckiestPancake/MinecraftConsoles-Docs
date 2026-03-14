# Biome.h / Biome.cpp

## Purpose
The base class for all biomes in Minecraft. It defines the climate (temperature, downfall), world generation features (trees, grass), and mob spawning rules for a specific region.

## Key Classes
- `Biome`: The main class for biome definitions.
- `Biome::MobSpawnerData`: Nested class for defining mob spawning weight and group sizes.

## Important Functions
- `staticCtor()`: Initializes all the default biomes (Plains, Desert, Forest, etc.).
- `getTreeFeature()` / `getGrassFeature()`: Returns the features used during the decoration phase.
- `getSkyColor()` / `getGrassColor()` / `getWaterColor()`: Returns the colors for the environment, often sourced from a color table (4J console specific).
- `getMobs()`: Returns the list of spawnable mobs for a given category.

## Modding Notes
- 4J Studios heavily modified the color system to use a centralized `ColourTable` instead of calculating it purely from temperature/downfall.
- New biomes like `jungle` and `jungleHills` are included.
- Relates to **world generation** and **entities** (spawning).

## Important Dependencies
- `BiomeDecorator.h`
- `MobCategory.h`
- `Feature.h`
- `WeighedRandom.h`

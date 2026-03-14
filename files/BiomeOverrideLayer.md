# BiomeOverrideLayer.h / BiomeOverrideLayer.cpp

## Purpose
A specialized world generation layer that allows for overriding the biome map with data from a binary file (`biomemap.bin`). This is likely used for fixed-map scenarios or special console edition modes.

## Key Classes
- `BiomeOverrideLayer`: Inherits from `Layer`.

## Important Functions
- `BiomeOverrideLayer()`: Loads the `biomemap.bin` file from the `GAME:\GameRules\` directory.
- `getArea()`: Returns biome data directly from the loaded binary map for the requested area.

## Modding Notes
- This is a console-specific feature (4J Studios). If the file is missing, it defaults to `Plains`.
- The override map size is fixed at 216x216.
- Relates to **world generation**.

## Important Dependencies
- `Layer.h`
- `Biome.h`
- `IntCache.h`

# AddSnowLayer

## Purpose
A world generation layer that introduces snow-covered biomes (Ice Flats) into the world during the biome generation process.

## Key Classes
- **AddSnowLayer**: Inherits from `Layer`.

## Important Functions
- `getArea()`: Randomly converts certain land biomes into snow biomes.

## Modding Notes
Simple randomization logic: if a cell is land, it has a 1/5 chance to become an `iceFlats` biome.

## Important Dependencies
- `Layer.h`
- `Biome.h`

[Category: Rendering]

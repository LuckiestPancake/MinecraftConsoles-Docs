# AddIslandLayer

## Purpose
A world generation layer responsible for adding islands to the ocean. It processes a 2D array of biome IDs and introduces land masses based on randomized rules.

## Key Classes
- **AddIslandLayer**: Inherits from `Layer` to implement island generation logic.

## Important Functions
- `getArea()`: Processes a specific region of the map, determining where land should be added based on neighboring cells and random chance.

## Modding Notes
This layer interacts with `Biome::iceFlats` and `Biome::frozenOcean` to handle cold climate island generation.

## Important Dependencies
- `Layer.h`
- `Biome.h`
- `IntCache.h`

[Category: Rendering]

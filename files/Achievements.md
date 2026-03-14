# Achievements

## Purpose
A registry and manager for all achievements in the game. It defines the layout of the achievement tree and provides static access to all achievement objects.

## Key Classes
- **Achievements**: Static container for all game achievements.

## Important Functions
- `staticCtor()`: Initializes all achievement objects, sets their positions, icons, and dependency requirements.
- `init()`: Placeholder for further initialization.

## Modding Notes
Contains many 4J-specific achievements and comments regarding console-specific releases (e.g., PS3, Xbox). It uses an offset `ACHIEVEMENT_OFFSET` (0x500000) for achievement IDs.

## Important Dependencies
- `Achievement.h`
- `Item.h`
- `Tile.h`

[Category: UI]

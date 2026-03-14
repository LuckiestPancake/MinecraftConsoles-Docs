# Achievement

## Purpose
Represents a single achievement in the game, including its requirements, display position on the achievement map, and icon.

## Key Classes
- **Achievement**: Inherits from `Stat` to represent an unlockable milestone.

## Important Functions
- `setAwardLocallyOnly()`: Sets the achievement to not sync with server awards.
- `setGolden()`: Marks the achievement as a "golden" (challenge) achievement.
- `postConstruct()`: Registers the achievement in the global `Achievements` list.
- `getDescription()`: Returns the localized description of the achievement.

## Modding Notes
4J Studios added flags like `isGoldenVar` and localized description support that integrates with their UI system.

## Important Dependencies
- `Stat.h`
- `ItemInstance.h`
- `Achievements.h`

[Category: UI]

# ArmorDyeRecipe

## Purpose
A specialized crafting recipe for dyeing leather armor. It handles combining leather armor with multiple dyes to produce a custom color.

## Key Classes
- **ArmorDyeRecipe**: Inherits from `Recipy`.

## Important Functions
- `matches()`: Checks if the crafting grid contains exactly one piece of leather armor and at least one dye.
- `assembleDyedArmor()`: Calculates the resulting RGB color by averaging the colors of all dyes and the existing armor color.
- `reqs()`: 4J added metadata for the recipe book/UI to display required ingredients.

## Modding Notes
The color averaging logic takes into account the "intensity" of the colors to produce more natural results when mixing many dyes.

## Important Dependencies
- `Recipy.h`
- `ArmorItem.h`
- `ItemInstance.h`

[Category: Entities]

# ArmorRecipes

## Purpose
A manager class that registers all standard armor crafting recipes (Helmets, Chestplates, etc.) for all materials.

## Key Classes
- **ArmorRecipes**: Handles bulk registration of armor recipes.

## Important Functions
- `addRecipes()`: Registers shaped recipes for all armor types using the standard "H", "U", and square patterns.
- `GetArmorType()`: Helper function to identify if an item ID corresponds to a helmet, chestplate, etc.

## Modding Notes
4J Studios removed the `Tile::fire` based chain armor recipe from the standard list as it wasn't craftable in the survival mode of the console edition.

## Important Dependencies
- `Recipes.h`
- `Item.h`

[Category: Entities]

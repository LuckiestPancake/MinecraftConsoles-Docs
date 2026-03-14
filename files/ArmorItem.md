# ArmorItem

## Purpose
Represents all types of wearable armor (Helmet, Chestplate, Leggings, Boots) made from various materials (Leather, Chain, Iron, Gold, Diamond). It handles protection values, durability, and dyeing for leather.

## Key Classes
- **ArmorItem**: The main class for armor items.
- **ArmorMaterial**: A nested class (or inner class) defining the properties of different armor types (durability, protection per slot, etc.).
- **ArmorDispenseItemBehavior**: Specialized dispenser behavior that allows dispensers to equip armor onto nearby mobs or players.

## Important Functions
- `getColor()`/`setColor()`: Handles custom RGB colors for leather armor.
- `getDefenseForSlot()`: Returns the protection points provided by this piece.
- `isValidRepairItem()`: Determines what item can be used in an anvil to repair this armor.
- `registerIcons()`: Loads icons, including overlays for dyed leather.

## Modding Notes
Includes constants for console-specific default leather colors. The `ArmorMaterial` class defines the "tier" of the armor.

## Important Dependencies
- `Item.h`
- `CompoundTag.h`
- `DispenserTile.h`

[Category: Entities]

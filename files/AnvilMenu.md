# AnvilMenu

## Purpose
Handles the logic for the Anvil UI, including item repairing, renaming, and enchantment combining. It calculates the "Enchantment Cost" (XP levels) required for operations.

## Key Classes
- **AnvilMenu**: Inherits from `AbstractContainerMenu`.

## Important Functions
- `createResult()`: The core logic that calculates the result of combining two items, including enchantment merging, repair amounts, and XP cost.
- `setItemName()`: Handles renaming the item in the anvil.
- `quickMoveStack()`: Handles shift-clicking items into and out of the anvil slots.
- `stillValid()`: Checks if the player is still near the anvil block.

## Modding Notes
Contains complex logic for enchantment compatibility and "tax" calculations. 4J Studios added `DEBUG_COST` prints for debugging the XP cost logic.

## Important Dependencies
- `AbstractContainerMenu.h`
- `EnchantmentHelper.h`
- `RepairContainer.h`
- `RepairResultSlot.h`

[Category: UI]

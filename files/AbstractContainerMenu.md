# AbstractContainerMenu

## Purpose
Provides the base logic for all inventory and container-based menus. It manages slots, item syncing between server and client, and handles various click types (pickup, quick move, swap, etc.).

## Key Classes
- **AbstractContainerMenu**: The abstract base class for all container menus (e.g., Chest, Crafting, Anvil).

## Important Functions
- `clicked()`: Processes various types of user interaction with slots.
- `broadcastChanges()`: Synchronizes slot changes to all listeners (e.g., players viewing the menu).
- `quickMoveStack()`: Handles "Shift-Click" or "Quick Move" logic for moving items between container and player inventory.
- `moveItemStackTo()`: Helper function to attempt to move an item stack into a range of slots.
- `getRedstoneSignalFromContainer()`: Calculates a redstone signal strength based on the container's contents.

## Modding Notes
4J Studios added several optimizations and bug fixes, such as `m_bNeedsRendered` for UI updates and `loopClick` to handle recursive quick-move bugs. It also includes 4J-specific container IDs.

## Important Dependencies
- `Player.h`
- `Slot.h`
- `ItemInstance.h`
- `ContainerListener.h`

[Category: UI]

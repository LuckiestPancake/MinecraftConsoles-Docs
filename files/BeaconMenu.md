# BeaconMenu.h / BeaconMenu.cpp

## Purpose
Handles the server-side logic and slot management for the Beacon block's user interface.

## Key Classes
- `BeaconMenu`: Inherits from `AbstractContainerMenu`.
- `BeaconMenu::PaymentSlot`: A specialized slot that only accepts beacon payment items (Emerald, Diamond, Gold, Iron).

## Important Functions
- `setData()`: Updates the beacon's levels and selected powers based on UI interactions.
- `quickMoveStack()`: Handles Shift-clicking items in/out of the beacon interface.
- `stillValid()`: Ensures the player is still close enough to the beacon to use it.

## Modding Notes
- Defines slot indices for the payment slot, main inventory, and hotbar.
- Relates to **UI** and **entities** (BeaconTileEntity).

## Important Dependencies
- `AbstractContainerMenu.h`
- `BeaconTileEntity.h`
- `Slot.h`

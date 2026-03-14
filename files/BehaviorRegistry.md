# Behavior.h / BehaviorRegistry.h / BehaviorRegistry.cpp

## Purpose
Provides a registry for "behaviors," specifically for the Dispenser block to determine how it handles different items when they are dispensed.

## Key Classes
- `Behavior`: A placeholder base class.
- `BehaviorRegistry`: A mapping of `Item*` to `DispenseItemBehavior*`.

## Important Functions
- `get()`: Retrieves the behavior for a specific item, or a default behavior if none is registered.
- `add()`: Registers a new behavior for an item.

## Modding Notes
- This system allows for extensible dispenser logic (e.g., shooting arrows vs. placing water).
- Relates to **blocks** (Dispenser) and **items**.

## Important Dependencies
- `DispenseItemBehavior.h`
- `Item.h`

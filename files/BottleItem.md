# BottleItem.h / BottleItem.cpp

## Purpose
The item class for the Glass Bottle. It handles the interaction of filling a bottle with water.

## Key Classes
- `BottleItem`: Inherits from `Item`.

## Important Functions
- `use()`: Performs a raycast. If it hits water, it consumes one bottle and gives the player a Water Potion.
- `TestUse()`: 4J Studios added this to show a tooltip when the player is looking at water while holding a bottle.

## Modding Notes
- Reuses the Potion item's icon.
- Relates to **items** and **alchemy**.

## Important Dependencies
- `Item.h`
- `ItemInstance.h`
- `HitResult.h`
- `Player.h`

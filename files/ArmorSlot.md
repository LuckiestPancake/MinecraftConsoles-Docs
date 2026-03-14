# ArmorSlot

## Purpose
A specialized UI slot used in the player's inventory to hold armor items. It enforces rules about which armor pieces can go into which slots.

## Key Classes
- **ArmorSlot**: Inherits from `Slot`.

## Important Functions
- `mayPlace()`: Only allows armor items that match the specific slot (e.g., only helmets in the head slot). Also allows pumpkins and skulls in the head slot.
- `getMaxStackSize()`: Always returns 1.
- `getNoItemIcon()`: Returns a "ghost" icon representing the empty slot (e.g., a helmet silhouette).

## Modding Notes
Created by 4J Studios to replace the anonymous class used in the original Java inventory menu for better structure.

## Important Dependencies
- `Slot.h`
- `ArmorItem.h`

[Category: UI]

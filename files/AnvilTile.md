# AnvilTile

## Purpose
Represents the Anvil block in the world. It is a "heavy" block that can fall and damage entities. It also provides the entry point for the Anvil UI.

## Key Classes
- **AnvilTile**: Inherits from `HeavyTile`.

## Important Functions
- `use()`: Opens the Anvil UI for the player.
- `falling()`: Sets the flag to hurt entities when the anvil falls.
- `onLand()`: Plays the anvil landing sound.
- `setPlacedBy()`: Determines the orientation of the anvil based on the player's direction.
- `getTexture()`: Returns different textures based on the anvil's damage state (Intact, Slightly Damaged, Very Damaged).

## Modding Notes
The damage state is stored in the block metadata (top 2 bits). The orientation is stored in the bottom 2 bits.

## Important Dependencies
- `HeavyTile.h`
- `AnvilMenu.h`

[Category: Entities]

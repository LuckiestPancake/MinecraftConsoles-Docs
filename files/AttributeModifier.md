# AttributeModifier.h / AttributeModifier.cpp

## Purpose
Represents a modification to an attribute's value, such as a percentage increase from a potion or a flat bonus from an item.

## Key Classes
- `AttributeModifier`: Handles the data and logic for modifying an attribute.
- `eMODIFIER_ID`: Enum for identifying specific types of modifiers (e.g., `eModifierId_POTION_MOVESPEED`).

## Important Functions
- `getOperation()`: Returns the operation type (Addition, Multiply Base, or Multiply Total).
- `getAmount()`: Returns the numerical amount of the modification.
- `isSerializable()`: Indicates if the modifier should be saved to NBT.
- `getHoverText()`: Generates a human-readable, formatted string for UI tooltips (e.g., "+20% Speed").

## Modding Notes
- 4J Studios replaced UUIDs and names with an `eMODIFIER_ID` enum for efficiency and consistency.
- `eModifierId_ANONYMOUS` is used for modifiers that don't need a fixed ID and cannot be easily removed by ID.
- Relates to **entities** and **UI**.

## Important Dependencies
- `HtmlString.h`
- `Attribute.h`

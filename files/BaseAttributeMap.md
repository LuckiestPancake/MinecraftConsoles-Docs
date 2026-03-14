# BaseAttributeMap.h / BaseAttributeMap.cpp

## Purpose
Manages a collection of `AttributeInstance` objects for an entity, providing methods to register, retrieve, and modify them.

## Key Classes
- `BaseAttributeMap`: A container class for managing all attributes on an entity.

## Important Functions
- `getInstance()`: Retrieves an `AttributeInstance` by its `Attribute` object or ID.
- `registerAttribute()`: Pure virtual function to register a new attribute in the map.
- `getAttributes()`: Returns a list of all attribute instances in the map.
- `addItemModifiers()` / `removeItemModifiers()`: 4J Studios added these to cleanly apply or remove attribute modifiers (like speed or health) granted by held or equipped items.

## Modding Notes
- The 4J implementation uses `eATTRIBUTE_ID` for efficient lookups in an `unordered_map`.
- Relates to **entities**.

## Important Dependencies
- `AttributeInstance.h`
- `ItemInstance.h`
- `ModifiableAttributeInstance.h`

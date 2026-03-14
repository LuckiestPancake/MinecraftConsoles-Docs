# AttributeInstance.h

## Purpose
Defines the interface for an attribute instance, which represents a specific attribute (like movement speed or attack damage) on an entity, including its base value and any active modifiers.

## Key Classes
- `AttributeInstance`: Abstract base class for managing a single attribute's value and its modifiers.

## Important Functions
- `getAttribute()`: Returns the underlying `Attribute` definition.
- `getBaseValue()` / `setBaseValue()`: Gets or sets the base value of the attribute before modifiers are applied.
- `getValue()`: Calculates and returns the final value of the attribute after applying all modifiers.
- `addModifier()` / `removeModifier()`: Manages `AttributeModifier` objects associated with this instance.
- `getModifiers()`: Retrieves the set of modifiers applied to this instance.

## Modding Notes
- This is a core part of the entity attribute system. Custom attributes or complex stat calculations would involve implementing or interacting with this interface.
- Relates to **entities**.

## Important Dependencies
- `AttributeModifier.h`
- `Attribute.h` (implied by `getAttribute()`)

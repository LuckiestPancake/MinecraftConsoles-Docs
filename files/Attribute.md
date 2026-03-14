# Attribute

## Purpose
Defines the interface for entity attributes (like health, movement speed, etc.). Attributes can have base values and modifiers.

## Key Classes
- **Attribute**: Interface for all attributes.
- **BaseAttribute**: A basic implementation of the Attribute interface.

## Important Functions
- `getName()`: Returns the unique name of the attribute.
- `getDefaultValue()`: Returns the default value for the attribute.

## Modding Notes
Used by the `AttributeInstance` class to track current values.

## Important Dependencies
- None

[Category: Entities]

# BaseAttribute.h / BaseAttribute.cpp

## Purpose
A base implementation of the `Attribute` interface, providing common functionality for entity attributes like default values and client synchronization settings.

## Key Classes
- `BaseAttribute`: Implements the core logic for an attribute definition.

## Important Functions
- `getId()`: Returns the `eATTRIBUTE_ID` for this attribute.
- `getDefaultValue()`: Returns the default starting value for the attribute.
- `isClientSyncable()`: Returns true if the attribute's value should be synchronized to clients.
- `setSyncable()`: Configures whether the attribute is synchronized to clients.

## Modding Notes
- This is the base class for more specific attribute types like `RangedAttribute`.
- Relates to **entities**.

## Important Dependencies
- `Attribute.h`

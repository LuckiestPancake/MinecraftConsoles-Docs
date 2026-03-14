# BasicTypeContainers.h / BasicTypeContainers.cpp

## Purpose
Provides C++ implementations of Java's primitive wrapper classes (Byte, Short, Integer, Float, Double) and some basic string utilities. This is used to maintain compatibility with original Minecraft logic that relies on these classes.

## Key Classes
- `Byte`, `Short`, `Integer`, `Float`, `Double`: Wrappers for primitive types with constants like `MAX_VALUE`.
- `_String`: A placeholder class used for type identification.

## Important Functions
- `Integer::parseInt()`: Converts a string to an integer with a specified radix.
- `Float::floatToIntBits()` / `Double::doubleToLongBits()`: Used for bitwise manipulation of floating-point numbers, often for networking or hashing.

## Modding Notes
- 4J Studios explicitly noted that `_String` should be used sparingly to avoid confusion with `std::string` or `std::wstring`.
- Includes platform-specific fixes (e.g., for PS3 NaN checks).
- Relates to **core utility**.

## Important Dependencies
- `<limits>`
- `<cmath>`

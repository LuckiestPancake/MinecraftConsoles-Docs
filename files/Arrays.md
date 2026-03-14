# Arrays

## Purpose
A utility class providing static methods for filling arrays with specific values. It works with various array types defined in the project.

## Key Classes
- **Arrays**: Static utility class.

## Important Functions
- `fill()`: Fills a range within an array (double, float, Biome*, byte) with a given value.

## Modding Notes
Uses `std::fill` internally but adds bounds checking via assertions.

## Important Dependencies
- `ArrayWithLength.h`

[Category: Utilities]

# ArrayWithLength

## Purpose
A simple wrapper for pointers that includes a length value, facilitating safer array management and easier passing of arrays with their size.

## Key Classes
- **arrayWithLength<T>**: Template class for 1D arrays.
- **array2DWithLength<T>**: Template class for 2D arrays.

## Important Functions
- `resize()`: Increases the size of the array while preserving existing data.
- `operator[]`: Provides indexed access to the underlying data.

## Modding Notes
Designed as a lightweight wrapper; it does not automatically delete its data in the destructor to allow for shallow copies without premature freeing of memory.

## Important Dependencies
- None (Standard C++ headers)

[Category: Utilities]

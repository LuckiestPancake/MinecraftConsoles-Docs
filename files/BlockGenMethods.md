# BlockGenMethods.h / BlockGenMethods.cpp

## Purpose
Provides static utility methods for placing primitive geometric shapes (boxes, frames, lines) of blocks in a 16x16 buffer. This is primarily used during world generation or structure generation.

## Key Classes
- `BlockGenMethods`: A stateless utility class.

## Important Functions
- `generateBox()`: Fills a rectangular volume with an "edge" block and a "filling" block.
- `generateFrame()`: Similar to `generateBox` but supports rotation (North, South, East, West).
- `generateLine()` / `generateDirectionLine()`: Draws a line of blocks between two points using a 3D version of Bresenham's line algorithm.

## Modding Notes
- These methods operate on raw `byteArray` block buffers, usually representing a chunk section.
- They handle rotation and coordinate clamping internally.
- Relates to **world generation**.

## Important Dependencies
- `ArrayWithLength.h`
- `Mth.h`
- `Level.h`

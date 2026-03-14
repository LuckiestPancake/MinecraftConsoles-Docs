# AABB

## Purpose
AABB (Axis-Aligned Bounding Box) is a fundamental class used for collision detection, spatial calculations, and intersection testing. It provides a way to represent a rectangular volume in 3D space aligned with the coordinate axes.

## Key Classes
- **AABB**: The main class representing the bounding box.
- **ThreadStorage**: A nested class added by 4J Studios to provide thread-local pools of AABB objects for improved performance and thread safety.

## Important Functions
- `newTemp()`: Retrieves a temporary AABB from the thread-local pool.
- `intersects()`: Checks if this AABB overlaps with another.
- `clipXCollide()`, `clipYCollide()`, `clipZCollide()`: Calculate the maximum movement allowed along an axis before collision with another AABB.
- `expand()`, `grow()`, `shrink()`: Modify the dimensions of the bounding box.
- `move()`: Translates the bounding box in 3D space.

## Modding Notes
4J Studios modified this class to include thread-local storage (`ThreadStorage`) to allow separate pools for different threads, which is a significant architectural change from the original Java version to handle console-specific threading models.

## Important Dependencies
- `Vec3.h`
- `Definitions.h`
- `HitResult.h`

[Category: Movement]
[Category: Entities]

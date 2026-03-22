# `AABB.h`

## Purpose
This header file declares the `AABB` (Axis-Aligned Bounding Box) class, which represents a rectangular volume in 3D space aligned with the coordinate axes. It is fundamental for collision detection, spatial queries, and determining intersection tests between objects or regions in the game world.

## Key Classes
- **`AABB`**: The main class representing the bounding box. It stores minimum and maximum coordinates along each axis (x, y, z).
- **`ThreadStorage`**: A nested class (added by 4J Studios) that manages thread-local pools of `AABB` objects. This is an optimization to improve performance and thread safety by reducing memory allocations and contention when `AABB` objects are frequently created and destroyed across multiple threads.

## Important Functions
- **`newTemp()`**: Retrieves a temporary `AABB` object from the thread-local pool managed by `ThreadStorage`. This is a performance optimization to avoid frequent heap allocations.
- **`intersects(const AABB &other)`**: Checks if this bounding box overlaps with another `AABB`.
- **`clipXCollide(const AABB &other, float xClip)`**: Calculates the maximum movement along the X-axis before this `AABB` collides with `other`.
- **`clipYCollide(const AABB &other, float yClip)`**: Calculates the maximum movement along the Y-axis before collision.
- **`clipZCollide(const AABB &other, float zClip)`**: Calculates the maximum movement along the Z-axis before collision.
- **`expand(float dx, float dy, float dz)`**: Expands the bounding box outwards by the specified amounts along each axis.
- **`grow(float dx, float dy, float dz)`**: Similar to `expand`, but often used to uniformly grow the box.
- **`shrink(float dx, float dy, float dz)`**: Shrinks the bounding box inwards.
- **`move(float dx, float dy, float dz)`**: Translates the bounding box by a given vector.
- **`getCenter(Vec3 &out)`**: Calculates and returns the center point of the bounding box.

## Modding Notes
- The `ThreadStorage` optimization is significant for performance, especially in multithreaded environments common in modern game engines. Modders could potentially leverage similar pooling strategies for other frequently created objects.
- The `clipXCollide`, `clipYCollide`, and `clipZCollide` functions are crucial for physics and collision response, providing precise collision response calculations.

## Important Dependencies
- **`Vec3.h`**: Likely used for vector operations and representing points/directions.
- **`Definitions.h`**: May contain common definitions or constants.
- **`HitResult.h`**: Potentially used for results of intersection tests.

## Category
- Collision Detection
- Math Utilities
- Spatial Partitioning
- Client-side / Server-side (used in both)

## Cross-references
- `Vec3`
- `HitResult`
- Used extensively by physics, rendering, and AI systems for spatial checks.

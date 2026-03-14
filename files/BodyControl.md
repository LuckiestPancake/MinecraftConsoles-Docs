# BodyControl

## Purpose
Manages the alignment and rotation of a mob's body relative to its head rotation. It handles smoothing and clamping of body rotation to ensure realistic movement and looking behavior.

## Key Classes
- **BodyControl**: A control class that inherits from `Control` and manages `LivingEntity` body rotation.

## Important Functions
- **clientTick()**: Updates the body rotation based on movement and head rotation. If moving, the body aligns to the movement direction. If stationary, the body eventually aligns with the head after a delay.
- **clamp(float clampTo, float clampFrom, float clampAngle)**: Helper function to restrict rotation within a specific angle range.

## Modding Notes
- The `maxClampAngle` is set to 75.0 degrees.
- There is a `timeStillBeforeTurn` constant (10 ticks) before the body starts to align with the head when stationary.

## Important Dependencies
- `LivingEntity`
- `Control`
- `MoveControl`
- `Mth` (Math utilities)

## Category
- Movement
- Entities

## Cross-references
- [[LivingEntity]]
- [[MoveControl]]
- [[Control]]

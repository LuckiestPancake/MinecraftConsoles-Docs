# FollowOwnerGoal

## Purpose
Governs the behavior of tamed animals (like Wolves or Cats) to follow their owner and teleport to them if they become too distant.

## Key Classes
* `FollowOwnerGoal`: The AI goal class for following owners.
* `TamableAnimal`: The tamed mob type.
* `LivingEntity`: The owner being followed.

## Important Functions
* `canUse()`: Checks if the owner exists, if the mob is not sitting, and if the distance to the owner exceeds the start threshold.
* `tick()`: Updates pathfinding to the owner and handles teleportation logic if the distance exceeds `TeleportDistance` (12 blocks).
* `start()`/`stop()`: Manages water avoidance settings during the follow behavior.

## Modding Notes
* 4J added `setLevel()` for schematic loading support.
* Teleportation logic includes a search for a solid block with space above it near the owner.
* Teleportation is disabled if the animal is currently leashed.

## Important Dependencies
* `TamableAnimal`
* `LivingEntity`
* `PathNavigation`
* `Level`

## Category
Entities / AI / Movement

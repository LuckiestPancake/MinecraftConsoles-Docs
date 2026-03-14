# Animal

## Purpose
The base class for all breedable, passive mobs (Cows, Sheep, Pigs, etc.). It handles breeding logic, "in love" states, and player interaction for taming/breeding.

## Key Classes
- **Animal**: Inherits from `AgableMob`.

## Important Functions
- `mobInteract()`: Handles feeding the animal to enter "in love" mode.
- `breedWith()`: Logic for spawning an offspring when two animals in love meet.
- `setInLove()`: Activates the breeding state and shows heart particles.
- `updateDespawnProtectedState()`: 4J added logic to prevent animals from despawning if they are "enclosed" (within a certain wander distance).

## Modding Notes
4J Studios added a significant "Despawn Protection" feature (`isDespawnProtected`) to ensure that animals in pens don't disappear, which was a common player request in the console editions.

## Important Dependencies
- `AgableMob.h`
- `Player.h`
- `ItemInstance.h`

[Category: Entities]

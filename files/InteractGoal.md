# InteractGoal

## Purpose
An extension of `LookAtPlayerGoal` that also requires the mob to stop moving, typically used for social or transactional interactions (like trading).

## Key Classes
* `InteractGoal`: The AI goal class for entity interaction.
* `LookAtPlayerGoal`: The base class providing looking logic.

## Important Functions
* `InteractGoal()`: Constructor that sets both `LookControlFlag` and `MoveControlFlag` to ensure the mob stops and stares.

## Modding Notes
* By requiring the `MoveControlFlag`, this goal prevents other movement-based goals from executing simultaneously.
* Commonly used for Villagers during trade sessions.

## Important Dependencies
* `Mob`
* `LookAtPlayerGoal`
* `Control`

## Category
Entities / AI

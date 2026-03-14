# AvoidPlayerGoal.h / AvoidPlayerGoal.cpp

## Purpose
An AI goal that causes a mob to flee from players or other specified entity types when they come within a certain range.

## Key Classes
- `AvoidPlayerGoal`: The main goal class.
- `AvoidPlayerGoalEntitySelector`: A helper class used to filter entities that the mob should avoid.

## Important Functions
- `canUse()`: Determines if the goal should start (e.g., is a player nearby and not tame?).
- `start()`: Initiates the pathfinding away from the target.
- `tick()`: Updates the mob's speed based on proximity to the avoided entity (sprinting if close).

## Modding Notes
- Used by ocelots to avoid players and creepers to avoid ocelots.
- Logic includes checks for `TamableAnimal` to ensure pets don't flee from their owners.
- Relates to **entities** and **movement**.

## Important Dependencies
- `Goal.h`
- `EntitySelector.h`
- `PathNavigation.h`
- `PathfinderMob.h`
- `RandomPos.h`

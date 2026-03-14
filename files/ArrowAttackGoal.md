# ArrowAttackGoal

## Purpose
An AI goal that allows a mob (like a Skeleton) to attack targets using a bow and arrows. It manages distancing and firing rates.

## Key Classes
- **ArrowAttackGoal**: Inherits from `Goal`.

## Important Functions
- `canUse()`: Determines if the mob should start using this goal.
- `tick()`: Logic for moving towards/away from the target and firing arrows.

## Modding Notes
Commonly used by ranged mobs.

## Important Dependencies
- `Goal.h`

[Category: Entities]

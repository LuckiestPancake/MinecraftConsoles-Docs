# AbsoptionMobEffect

## Purpose
Handles the "Absorption" status effect, which provides players or entities with extra temporary health points.

## Key Classes
- **AbsoptionMobEffect**: Inherits from `MobEffect` to implement specific absorption logic.

## Important Functions
- `addAttributeModifiers()`: Adds the absorption health (4 points per amplifier level) to the entity when the effect is applied.
- `removeAttributeModifiers()`: Removes the absorption health when the effect expires or is cleared.

## Modding Notes
Directly interacts with `LivingEntity::setAbsorptionAmount` to manage the temporary health buff.

## Important Dependencies
- `MobEffect.h`
- `LivingEntity.h`

[Category: Entities]

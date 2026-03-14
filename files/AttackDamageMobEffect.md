# AttackDamageMobEffect

## Purpose
Handles status effects that modify an entity's attack damage, such as "Strength" or "Weakness".

## Key Classes
- **AttackDamageMobEffect**: Inherits from `MobEffect`.

## Important Functions
- `getAttributeModifierValue()`: Calculates the damage bonus/penalty based on the effect amplifier.

## Modding Notes
Modifies the `SharedMonsterAttributes::ATTACK_DAMAGE` attribute.

## Important Dependencies
- `MobEffect.h`

[Category: Entities]

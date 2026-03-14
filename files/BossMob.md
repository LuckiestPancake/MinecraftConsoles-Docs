# BossMob

## Purpose
Provides an interface and base functionality for boss-type mobs (like the Ender Dragon or Wither).

## Key Classes
- **BossMob**: An interface (in `.h`) and a base class (in `.cpp`) for boss mobs.

## Important Functions
- **getMaxHealth()**: Returns the maximum health of the boss.
- **getHealth()**: Returns current health.
- **getAName()**: Returns the name of the boss for the boss bar.
- **hurt(DamageSource *source, int damage)**: Handles taking damage.
- **reallyHurt(DamageSource *source, int damage)**: Performs the actual damage application.

## Modding Notes
- The header defines a pure virtual interface, while the implementation seems to provide a base for boss entities.
- Initial health is set to 100 in the base constructor.

## Important Dependencies
- `Mob`
- `Level`
- `DamageSource`
- `BossMobPart`

## Category
- Entities

## Cross-references
- [[Mob]]
- [[EnderDragon]]
- [[WitherBoss]]

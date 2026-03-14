# Boat.h / Boat.cpp

## Purpose
Implements the Boat entity, a vehicle used for water transportation. It handles buoyancy, player control, collision breakage, and interpolation for networking.

## Key Classes
- `Boat`: Inherits from `Entity`.

## Important Functions
- `tick()`: Updates the boat's position, handles buoyancy (bobbing), gravity, and player input.
- `hurt()`: Manages damage from players or environment. 4J Studios added a check to prevent "untrusted" players from breaking boats.
- `interact()`: Handles players entering or exiting the boat.
- `lerpTo()` / `lerpMotion()`: Handles smooth movement synchronization between server and client.
- `createSplash()`: Generates water particle effects based on speed.

## Modding Notes
- Boats in this version break into 3 wood planks and 2 sticks if they hit a solid block at high speed.
- 4J Studios added a `MAX_XBOX_BOATS` limit to prevent performance issues.
- Relates to **entities** and **movement**.

## Important Dependencies
- `Entity.h`
- `Player.h`
- `DamageSource.h`
- `Level.h`
- `Mth.h`
- `Item.h`

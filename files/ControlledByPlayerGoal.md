# ControlledByPlayerGoal

## Purpose
Allows a player to control a mob's movement, specifically designed for riding animals like pigs using a "carrot on a stick."

## Key Classes
* `ControlledByPlayerGoal`: The main goal class for player-controlled mob movement.
* `Mob`: The entity being controlled.
* `PathfinderMob`: Used for movement and jump controls.

## Important Functions
* `canUse()`: Checks if the mob has a player rider and if the control conditions (like boosting or holding a carrot on a stick) are met.
* `tick()`: Processes player input to steer the mob and handles movement/jumping physics.
* `boost()`: Initiates a temporary speed increase for the mob.

## Modding Notes
* 4J added a `walkSpeed` parameter to ensure the mob has a base speed when ridden.
* Handles the durability of the "carrot on a stick" and replaces it with a regular fishing rod when broken.
* Implements specific jump-ahead logic to allow the mob to navigate terrain while being steered.

## Important Dependencies
* `Mob`
* `Player`
* `PathfinderMob`
* `ItemInstance` (Carrot on a stick)
* `Mth` (Math utilities)

## Category
Movement / AI

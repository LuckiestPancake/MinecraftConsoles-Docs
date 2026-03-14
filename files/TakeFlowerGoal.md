# TakeFlowerGoal

## Purpose
An AI goal for baby Villagers to respond to an Iron Golem offering a poppy flower, creating a social interaction between the two.

## Key Classes
* `TakeFlowerGoal`: The AI goal class for accepting flowers.
* `Villager`: The baby villager recipient.
* `VillagerGolem`: The golem offering the flower.

## Important Functions
* `canUse()`: Triggers for baby villagers during the day if an Iron Golem in the vicinity is currently offering a flower.
* `tick()`: Directs the baby villager to walk towards the Golem and eventually "take" the flower, which resets the Golem's offering state.

## Modding Notes
* This goal is the reciprocal behavior to `OfferFlowerGoal`.
* The baby villager waits for a random `pickupTick` before moving towards the Golem to make the interaction feel more natural.

## Important Dependencies
* `Villager`
* `VillagerGolem`
* `Level`

## Category
Entities / AI / Movement

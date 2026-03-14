# OfferFlowerGoal

## Purpose
A peaceful interaction AI goal for Villager Golems (Iron Golems) where they offer a poppy flower to nearby Villagers.

## Key Classes
* `OfferFlowerGoal`: The AI goal class.
* `VillagerGolem`: The entity offering the flower.
* `Villager`: The recipient of the gesture.

## Important Functions
* `canUse()`: Triggers rarely (1 in 8000 chance) during the day when a villager is within 6 blocks.
* `start()`: Activates the `offerFlower` state on the Iron Golem, which typically triggers a specific animation or item display.
* `tick()`: Causes the Golem to maintain eye contact with the villager for the duration of the goal (400 ticks).

## Modding Notes
* This behavior is purely cosmetic and does not affect village reputation or villager behavior.
* The 400-tick duration is defined as `OFFER_TICKS`.

## Important Dependencies
* `VillagerGolem`
* `Villager`
* `Level`
* `Control`

## Category
Entities / AI

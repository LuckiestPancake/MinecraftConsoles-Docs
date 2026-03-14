# Chicken

## Purpose
The `Chicken` class represents the Chicken mob in the game. Chickens are passive, farm animals that lay eggs periodically and drop feathers and meat upon death. They are known for their flapping animation and relatively weak AI.

## Key Classes
- `Animal`: The base class for animal mobs.
- `Entity`: The base class for all game entities.
- `Level`: Represents the game world.
- `CompoundTag`: Used for reading and writing entity data to save files.
- `Item`: Represents items in the game, used for loot drops and breeding food.
- `SharedMonsterAttributes`: For defining entity attributes like health and movement speed.
- `AgableMob`: Base class for mobs that can breed.
- `MobCategory`: Enum for classifying mobs.

## Important Functions
- `Chicken(Level *level)`: Constructor for the Chicken. Initializes its state, sets size, and populates its AI goal selector with behaviors like fleeing, breeding, finding food, following parents, and general wandering.
- `registerAttributes()`: Sets the maximum health and movement speed for the Chicken.
- `aiStep()`: The main AI update function. It handles the chicken's flapping animation, its falling behavior, and periodically lays eggs if it's an adult.
- `causeFallDamage(float distance)`: Overridden to do nothing, as chickens are immune to fall damage.
- `getAmbientSound()`, `getHurtSound()`, `getDeathSound()`: Returns the sound IDs for the chicken's ambient, hurt, and death sounds.
- `playStepSound(int xt, int yt, int zt, int t)`: Plays a subtle step sound for the chicken.
- `getDeathLoot()`: Returns the item ID for feathers.
- `dropDeathLoot(...)`: Spawns feathers and cooked or raw chicken upon death, depending on whether the chicken was on fire.
- `getBreedOffspring(shared_ptr<AgableMob> target)`: Creates a new Chicken entity if the game can support more, used during breeding.
- `isFood(shared_ptr<ItemInstance> itemInstance)`: Checks if a given item can be used to feed and breed chickens (wheat seeds, melon seeds, pumpkin seeds, nether wart seeds).

## Modding Notes
- The `eggTime` variable controls how often chickens lay eggs. This can be adjusted for more or less frequent egg-laying.
- The `flap`, `flapSpeed`, `flapping`, `oFlapSpeed`, and `oFlap` variables control the flapping animation. Modifying these could alter the visual appearance of the chicken's movement.
- The `dropDeathLoot` function can be modified to change the items dropped by chickens, or their quantities.
- The `isFood` function determines which items can be used for breeding. This can be extended to include other food items.
- The `registerAttributes` function sets the base movement speed and health.

## Important Dependencies
- `Animal.h`: Inherits from `Animal` for general animal mob properties.
- `net.minecraft.world.entity.ai.goal.h`: For AI goal definitions.
- `net.minecraft.world.item.h`: For item IDs (seeds, feathers, chicken meat).
- `net.minecraft.world.entity.ai.attributes.h`: For entity attributes.
- `SoundTypes.h`: For sound constants.

**Cross-references:**
- AI/Behavior: `aiStep()`, `useNewAi()`, `PanicGoal`, `BreedGoal`, `TemptGoal`, `FollowParentGoal`, `RandomStrollGoal`, `LookAtPlayerGoal`, `RandomLookAroundGoal`
- Entities: `Animal`, `AgableMob`, `Player`
- World Interaction: `causeFallDamage()`, `playStepSound()`, `level->canCreateMore()`
- Items: `Item::seeds_wheat_Id`, `Item::egg->id`, `Item::feather_Id`, `Item::chicken_cooked_Id`, `Item::chicken_raw_Id`
- Sounds: `getAmbientSound()`, `getHurtSound()`, `getDeathSound()`, `playStepSound()`
- Data Handling: `registerAttributes()`, `dropDeathLoot()`

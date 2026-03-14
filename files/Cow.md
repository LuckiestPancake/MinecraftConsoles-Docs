# Cow

## Purpose
The `Cow` class represents the Cow mob in the game. Cows are passive farm animals that drop leather and beef when killed. They can also be milked by players using an empty bucket.

## Key Classes
- `Animal`: The base class for animal mobs.
- `Entity`: The base class for all game entities.
- `Level`: Represents the game world.
- `Player`: Represents a player entity.
- `CompoundTag`: Used for reading and writing entity data to save files.
- `Item`: Represents items in the game, used for loot drops and breeding.
- `SharedMonsterAttributes`: For defining entity attributes like health and movement speed.
- `AgableMob`: Base class for mobs that can breed.
- `MobCategory`: Enum for classifying mobs.

## Important Functions
- `Cow(Level *level)`: Constructor for the Cow. Initializes its size, sets up its AI goals (fleeing, breeding, eating wheat, following parent, wandering, looking at player), and ensures it avoids water.
- `registerAttributes()`: Sets the maximum health and movement speed for the Cow.
- `getAmbientSound()`, `getHurtSound()`, `getDeathSound()`: Returns the sound IDs for the cow's ambient, hurt, and death sounds.
- `playStepSound(int xt, int yt, int zt, int t)`: Plays a step sound for the cow.
- `getSoundVolume()`: Returns the volume for the cow's sounds.
- `getDeathLoot()`: Returns the item ID for leather.
- `dropDeathLoot(...)`: Spawns leather and cooked or raw beef upon death, depending on whether the cow was on fire.
- `mobInteract(shared_ptr<Player> player)`: Handles player interaction with the cow. If the player is holding an empty bucket and the cow is not in creative mode, the cow is milked, and the player receives a milk bucket. It also increments the player's "cowsMilked" statistic.
- `getBreedOffspring(shared_ptr<AgableMob> target)`: Creates a new Cow entity if the game can support more, used during breeding.

## Modding Notes
- The `registerAttributes()` function controls the Cow's health and movement speed.
- The `dropDeathLoot()` function can be modified to change the items dropped by cows or their quantities.
- The `mobInteract()` function can be modified to alter milking mechanics or add other player interactions.
- The `isFood()` function (inherited from `Animal` and potentially overridden or checked implicitly by `TemptGoal`) determines what items can be used for breeding.

## Important Dependencies
- `Animal.h`: Inherits from `Animal` for general animal mob properties.
- `net.minecraft.world.entity.ai.goal.h`: For AI goal definitions.
- `net.minecraft.world.entity.ai.navigation.h`: For navigation capabilities (like avoiding water).
- `net.minecraft.world.item.h`: For item IDs (wheat, empty bucket, milk bucket, leather, beef).
- `net.minecraft.world.entity.player.h`: For player interaction.
- `SoundTypes.h`: For sound constants.

**Cross-references:**
- AI/Behavior: `registerAttributes()`, `getAmbientSound()`, `getHurtSound()`, `getDeathSound()`, `playStepSound()`, `mobInteract()`, `getBreedOffspring()`, `TemptGoal`, `BreedGoal`, `FollowParentGoal`, `PanicGoal`, `RandomStrollGoal`, `LookAtPlayerGoal`, `RandomLookAroundGoal`
- Entities: `Animal`, `Player`, `AgableMob`
- Items: `Item::wheat_Id`, `Item::bucket_empty->id`, `Item::bucket_milk`, `Item::leather_Id`, `Item::beef_raw_Id`, `Item::beef_cooked_Id`
- World Interaction: `mobInteract()`, `dropDeathLoot()`
- Data Handling: `registerAttributes()`, `dropDeathLoot()`

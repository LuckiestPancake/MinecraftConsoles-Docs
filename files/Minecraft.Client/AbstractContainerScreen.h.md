# `AbstractContainerScreen.h`

## Purpose
This header file declares the `AbstractContainerScreen` class, which serves as the abstract base class for all GUI screens that manage inventories and containers in the game. It defines the interface for rendering container elements, handling player input, and managing the screen's lifecycle.

## Key Classes
- **`AbstractContainerScreen`**: The main class, inheriting from `Screen`. It manages the associated `AbstractContainerMenu`, the `ItemRenderer` for displaying items, and player interaction logic.
- **`Screen`**: The base class for all game screens.
- **`ItemRenderer`**: Used for rendering item icons within the GUI.
- **`AbstractContainerMenu`**: Represents the game's logic for inventory management, which this screen visualizes.
- **`Slot`**: Represents an individual slot within the container GUI.
- **`Container`**: The underlying game object that the menu represents.

## Important Functions
- **`init()`**: Initializes the screen, setting up the menu and positioning the GUI elements based on screen dimensions and image width/height.
- **`render(int xm, int ym, float a)`**: The virtual function for rendering the screen. It's intended to draw the background, slots, items, and potentially tooltips. (Note: Much of the implementation is commented out, suggesting it's a base class structure).
- **`renderLabels()`**: A virtual function intended for rendering text labels on the screen.
- **`renderBg(float a)`**: A pure virtual function that derived classes must implement to draw the specific background of their container.
- **`renderSlot(Slot *slot)`**: Renders a single inventory slot, including its item if present.
- **`findSlot(int x, int y)`**: Helper function to determine which `Slot` is under the mouse cursor.
- **`isHovering(Slot *slot, int xm, int ym)`**: Checks if the mouse is currently over a specific slot.
- **`mouseClicked(int x, int y, int buttonNum)`**: Handles mouse button clicks within the screen, delegating inventory interactions to the `GameMode`.
- **`mouseReleased(int x, int y, int buttonNum)`**: Handles mouse button releases.
- **`keyPressed(wchar_t eventCharacter, int eventKey)`**: Handles keyboard input, typically for closing the screen.
- **`removed()`**: Called when the screen is closed.
- **`slotsChanged(shared_ptr<Container> container)`**: Called when the container's slots are modified.
- **`isPauseScreen()`**: Indicates if this screen should pause the game.
- **`tick()`**: Called every game tick to update the screen's state, including checking if the container should remain open.

## Modding Notes
- This is an abstract base class, meaning derived classes (like `ChestScreen`, `AnvilScreen`) will implement the `renderBg` function and potentially override others.
- The `itemRenderer` is a static member, indicating a shared instance for all screens.

## Important Dependencies
- `Screen.h`: Base class for all screens.
- `ItemRenderer.h`
- `AbstractContainerMenu.h`
- `Slot.h`
- `Container.h`
- `..\Minecraft.World
et.minecraft.world.inventory.h` (implied by `AbstractContainerMenu` and `Slot`)
- `..\Minecraft.World
et.minecraft.locale.h` (implied by usage in `.cpp`)
- `..\Minecraft.World
et.minecraft.world.item.h` (implied by usage in `.cpp`)

## Category
- UI
- Client-side Rendering

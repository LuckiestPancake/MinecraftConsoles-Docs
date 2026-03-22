# `AbstractTexturePack.cpp`

## Purpose
This file implements the `AbstractTexturePack` class, which is a foundational class for managing texture packs in the game. It provides an abstract interface for loading resources (like icons, descriptions, and animation data) from a texture pack, whether it's from a file, an archive, or a DLC. It defines methods for loading, unloading, and accessing resources, along with handling fallback mechanisms for missing files.

## Key Classes
- **`AbstractTexturePack`**: The abstract base class for all texture pack implementations. It manages the texture pack's ID, name, fallback pack, and associated resources.
- **`File`**: Represents a file in the filesystem.
- **`InputStream` / `BufferedReader` / `InputStreamReader`**: Classes for reading data from files or archives.
- **`wstring`**: Standard C++ wide string for handling text.
- **`Textures`**: A class likely responsible for managing OpenGL texture IDs.
- **`ColourTable`**: Used for loading color definitions from files, potentially for UI elements or biome coloring.
- **`BufferedImage`**: Represents image data.

## Important Functions
- **`AbstractTexturePack(DWORD id, File *file, const wstring &name, TexturePack *fallback)`**: Constructor that initializes the texture pack with an ID, file handle, name, and an optional fallback pack.
- **`trim(wstring line)`**: Utility function to truncate strings, likely for description lines.
- **`loadIcon()` / `loadComparison()`**: Platform-specific (Xbox) functions to load icon and comparison image data from resources.
- **`loadDescription()`**: Reads `pack.txt` to get description lines for the texture pack (currently commented out).
- **`getResource(const wstring &name, bool allowFallback)`**: Attempts to retrieve a resource stream for a given file name. If not found directly, it tries the `fallback` pack if `allowFallback` is true.
- **`unload(Textures *textures)`**: Releases any loaded textures associated with this pack.
- **`load(Textures *textures)`**: Loads the texture pack's icon into OpenGL, creating a texture ID if necessary.
- **`hasFile(const wstring &name, bool allowFallback)`**: Checks if a specific file exists within this texture pack or its fallback.
- **`getId()` / `getName()` / `getWorldName()` / `getDesc1()` / `getDesc2()`**: Accessors for texture pack properties.
- **`getAnimationString(const wstring &textureName, const wstring &path, bool allowFallback)`**: Retrieves animation definitions from `.txt` files associated with textures.
- **`getImageResource(...)`**: Loads image data from a file path into a `BufferedImage` object.
- **`loadDefaultUI()` / `loadColourTable()` / `loadDefaultHTMLColourTable()`**: Functions related to loading UI skins and color tables, with platform-specific implementations.

## Modding Notes
- The `loadIcon` and `loadComparison` functions are platform-specific (`_XBOX`) and use `XuiResourceLoadAllNoLoc`.
- The `loadDescription` function is commented out but shows how to read a `pack.txt` file.
- The `getResource` method's fallback mechanism is important for managing multiple texture packs or default assets.
- `loadUI()` and `loadColourTable()` suggest extensibility for custom UI elements and color schemes.

## Important Dependencies
- `Textures.h`: For texture management.
- `..\Minecraft.World\InputOutputStream.h`: For file I/O operations.
- `..\Minecraft.World\StringHelpers.h`: For string manipulation.
- `Common/UI/UI.h`: For UI-related functionality.
- `Windows.h` (via `stdafx.h`): For `DWORD`, `GetModuleHandle`.
- `XuiResourceLoadAllNoLoc`, `XuiFree`, `XuiSceneCreate`, etc. (Xbox-specific XUI functions).
- `GL/gl.h` (via includes): For OpenGL texture binding.

## Category
- Asset Management
- Texture Packs
- UI
- Client-side Resources

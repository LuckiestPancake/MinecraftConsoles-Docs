# `AbstractTexturePack.h`

## Purpose
This header file declares the `AbstractTexturePack` class, which serves as an abstract base class for managing texture packs. It defines the interface for loading resources like icons, descriptions, animation definitions, and raw image data from various sources (files, archives, DLCs). It also includes functionality for managing OpenGL texture IDs and platform-specific UI loading.

## Key Classes
- **`AbstractTexturePack`**: The core abstract class providing the interface for texture pack operations. It manages an ID, name, fallback pack, file handle, and associated resources.
- **`TexturePack`**: An abstract base class or interface that `AbstractTexturePack` inherits from.
- **`File`**: Represents a file system object.
- **`InputStream`, `BufferedReader`, `InputStreamReader`**: For reading data streams.
- **`wstring`**: Standard C++ wide string type.
- **`Textures`**: Likely manages OpenGL texture IDs.
- **`BufferedImage`**: Represents image data.
- **`ColourTable`**: Manages color definitions for UI elements or game rendering.
- **`ArchiveFile`**: Represents compressed archive files.
- **`DLCPack`**: Represents data from Downloadable Content packs.

## Important Functions
- **`AbstractTexturePack(DWORD id, File *file, const wstring &name, TexturePack *fallback)`**: Constructor to initialize a texture pack with an ID, file access, name, and a fallback pack.
- **`trim(wstring line)`**: Utility to truncate strings, likely for description lines.
- **`loadIcon()` / `loadComparison()`**: Platform-specific (`_XBOX`) methods to load icon and comparison image data from resources.
- **`loadDescription()`**: Reads a `pack.txt` file for texture pack descriptions (currently commented out).
- **`getResource(const wstring &name, bool allowFallback)`**: Retrieves a resource stream. If not found locally, it uses the fallback pack if `allowFallback` is true.
- **`unload(Textures *textures)`**: Releases OpenGL textures associated with this pack.
- **`load(Textures *textures)`**: Loads the texture pack's icon into OpenGL.
- **`hasFile(const wstring &name, bool allowFallback)`**: Checks for the existence of a file within the pack or its fallback.
- **`getId()` / `getName()` / `getDesc1()` / `getDesc2()` / `getWorldName()`**: Accessors for texture pack properties.
- **`getAnimationString(...)`**: Retrieves animation definitions from `.txt` files.
- **`getImageResource(...)`**: Loads image data into a `BufferedImage`.
- **`loadDefaultUI()` / `loadColourTable()` / `loadDefaultHTMLColourTable()`**: Handles loading UI skins and color definitions, with platform-specific implementations.
- **`getXuiRootPath()`**: Returns a platform-specific root path for XUI resources.
- **`getPackIcon()` / `getPackComparison()`**: Returns raw image data for the pack's icon and comparison image.
- **`getDLCPack()`**: Pure virtual function to retrieve the DLC pack object.
- **`getResourceImplementation(...)`**: Pure virtual function to be implemented by derived classes for resource loading.
- **`hasFile(const wstring &name)`**: Pure virtual function to be implemented by derived classes to check for file existence.

## Modding Notes
- This class is abstract and requires derived classes to implement pure virtual functions like `getResourceImplementation`, `hasFile`, and `getDLCPack`.
- Includes platform-specific code for Xbox (`_XBOX`) and PS3 (`__PS3__`) related to resource loading and UI.
- The use of `DWORD`, `WCHAR`, and Windows-specific API calls (`GetModuleHandle`) indicates a strong Windows/console dependency.

## Important Dependencies
- `TexturePack.h`: Base class/interface.
- `Textures.h`: For texture management.
- `..\Minecraft.World\InputOutputStream.h`: For I/O operations.
- `..\Minecraft.World\StringHelpers.h`: For string utilities.
- `Common/UI/UI.h`: For UI functions.
- `Windows.h` (via `stdafx.h`): For Windows types like `DWORD`, `ULONG_PTR`, `WCHAR`.
- `GL/gl.h` (via `Textures.h`): For OpenGL texture binding.
- XUI library functions (e.g., `XuiResourceLoadAllNoLoc`, `XuiElementGetId`) for Xbox platform.

## Category
- Asset Management
- Texture Packs
- UI
- Client-side Resources

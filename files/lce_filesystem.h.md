# lce_filesystem.h

## Purpose
Header file declaring utility functions for filesystem operations, currently focused on Windows 64-bit platforms.

## Key Classes
None.

## Important Functions
- `FileOrDirectoryExists(const char* path)`: Checks if the specified path exists as either a file or a directory.
- `FileExists(const char* path)`: Checks if the specified path exists and is a file.
- `DirectoryExists(const char* path)`: Checks if the specified path exists and is a directory.
- `GetFirstFileInDirectory(const char* directory, char* outFilePath, size_t outFilePathSize)`: Finds the first file in a directory and returns its full path.

## Modding Notes
These functions are useful for modders who need to verify the existence of custom resource files or directories before loading them.

## Important Dependencies
- `stdafx.h` (indirectly via implementation)
- `windows.h` (for Windows implementation)

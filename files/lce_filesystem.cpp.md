# lce_filesystem.cpp

## Purpose
Implementation of the filesystem utility functions defined in `lce_filesystem.h`, providing Windows-specific wrappers for filesystem checks.

## Key Classes
None.

## Important Functions
- `FileOrDirectoryExists`: Uses `GetFileAttributesA` to verify existence.
- `FileExists`: Checks attributes to ensure the path is not a directory.
- `DirectoryExists`: Checks attributes to ensure the path is a directory.
- `GetFirstFileInDirectory`: Uses `FindFirstFileA` and `FindNextFileA` Win32 APIs to find the first non-directory entry in a folder.

## Modding Notes
The implementation is currently restricted to Windows (`_WINDOWS64`). Any modding that requires cross-platform support would need to extend these functions.

## Important Dependencies
- `stdafx.h`
- `lce_filesystem.h`
- `windows.h`
- `stdio.h`

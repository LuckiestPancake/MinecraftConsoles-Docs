# AdminLogCommand

## Purpose
An interface for logging administrative commands. This is likely used for auditing actions taken by operators or through the console.

## Key Classes
- **AdminLogCommand**: An abstract interface defining `logAdminCommand`.

## Important Functions
- `logAdminCommand()`: Logs an admin action with details like source, type, message, and custom data.

## Modding Notes
Implemented by classes that handle command execution and logging (e.g., server console or player command handlers).

## Important Dependencies
- `ChatPacket.h`
- `CommandSender.h`

[Category: UI]
[Category: Networking]

# BinaryHeap.h / BinaryHeap.cpp

## Purpose
A standard binary heap data structure, specifically optimized for use in the pathfinding algorithm (A*). It stores `Node` objects and sorts them by their cost (`f` value).

## Key Classes
- `BinaryHeap`: Manages an array of `Node` pointers in a min-heap structure.

## Important Functions
- `insert()`: Adds a new node and bubbles it up.
- `pop()`: Removes and returns the node with the lowest cost.
- `changeCost()`: Updates a node's cost and re-sorts the heap efficiently.
- `upHeap()` / `downHeap()`: Internal methods for maintaining the heap property.

## Modding Notes
- This is a performance-critical part of the pathfinding system.
- 4J Studios implemented it with a `NodeArray` (likely a wrapper around `Node**`) for efficiency.
- Relates to **movement** (AI pathfinding).

## Important Dependencies
- `Node.h`
- `BasicTypeContainers.h`

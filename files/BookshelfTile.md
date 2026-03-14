# BookshelfTile

## Purpose
Represents the Bookshelf block, handling its appearance and the items it drops when destroyed.

## Key Classes
- **BookshelfTile**: Inherits from `Tile`.

## Important Functions
- **getTexture(int face, int data)**: Returns the wood texture for the top and bottom faces, and the bookshelf texture for the sides.
- **getResourceCount(Random *random)**: Returns 3 (the number of books dropped).
- **getResource(int data, Random *random, int playerBonusLevel)**: Returns `Item::book_Id`.

## Modding Notes
- Uses `Material::wood`.
- Drops books instead of the block itself when broken (unless Silk Touch is used, though not explicitly handled in this snippet).

## Important Dependencies
- `Tile`
- `Material`
- `Item`

## Category
- Entities (Tiles)

## Cross-references
- [[Tile]]
- [[BookItem]]

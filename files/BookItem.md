# BookItem

## Purpose
Represents the Book item in Minecraft, handling its properties and enchantment capabilities.

## Key Classes
- **BookItem**: Inherits from `Item`.

## Important Functions
- **isEnchantable(shared_ptr<ItemInstance> itemInstance)**: Books are enchantable if the stack count is 1.
- **getEnchantmentValue()**: Returns the base enchantment value (1 for books).

## Modding Notes
- Books are used in crafting bookshelves and as a base for enchanted books.

## Important Dependencies
- `Item`
- `ItemInstance`

## Category
- Entities (Items)

## Cross-references
- [[Item]]
- [[EnchantedBookItem]]

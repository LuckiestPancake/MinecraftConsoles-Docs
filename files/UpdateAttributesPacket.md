# UpdateAttributesPacket

## Purpose
The `UpdateAttributesPacket` synchronizes an entity's attributes (such as movement speed, follow range, or health) and their active modifiers from the server to the client.

## Key Classes
- **UpdateAttributesPacket**: The main packet class.
- **AttributeSnapshot**: A nested class representing a captured state of an attribute.
- **AttributeInstance**: The actual attribute object on the entity.
- **AttributeModifier**: Modifiers that affect the base value of an attribute.

## Important Functions
- **read(DataInputStream *dis)**: Reads the entity ID and a list of attributes, each with its own list of modifiers.
- **write(DataOutputStream *dos)**: Writes the full attribute and modifier set.
- **handle(PacketListener *listener)**: Dispatches to `handleUpdateAttributes`.

## Modding Notes
- This is a complex packet that ensures the client correctly calculates entity properties that are affected by potions, enchantments, or specific mob traits.
- Categorized under **Entities** and **Networking**.

## Important Dependencies
- `Packet.h`
- `net.minecraft.world.entity.ai.attributes.h`

---
**Related to:** [Entities](Entities.md), [Networking](Networking.md)

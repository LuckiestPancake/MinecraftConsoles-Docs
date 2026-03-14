# TradeItemPacket

## Purpose
The `TradeItemPacket` is a 4J-specific packet likely used to communicate the selection of a specific trade offer when interacting with a Villager.

## Key Classes
- **TradeItemPacket**: The packet class for trading interactions.

## Important Functions
- **read(DataInputStream *dis)**: Reads the container ID and the index of the trade offer.
- **write(DataOutputStream *dos)**: Writes the trading data.
- **handle(PacketListener *listener)**: Dispatches to `handleTradeItem`.

## Modding Notes
- Contains `containerId` to ensure the trade is being applied to the correct open merchant window.
- Categorized under **UI** and **Networking**.

## Important Dependencies
- `Packet.h`
- `PacketListener.h`

---
**Related to:** [UI](UI.md), [Networking](Networking.md)

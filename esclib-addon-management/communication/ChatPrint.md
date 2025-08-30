# ChatPrint

## Usage example
```lua
addon:ChatPrint(player, "Hello World")
addon:ChatPrint({player1, player2}, "Message for multiple players")
```

## Args:
1. **Player|table** recievers - Single player or table of players to send message to
2. **any** ... - Variable number of arguments to send

## Notes
Sends a formatted chat message to specified players. On client, first argument is treated as message content. Automatically formats with addon name and color.

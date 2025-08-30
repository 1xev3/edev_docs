# RegisterServerSettings

## Usage example
```lua
addon:RegisterServerSettings({
    ["Server"] = {
        vars = {
            ["max_players"] = {value = 64, type = "number"}
        }
    }
})
```

## Args:
1. **table** settings - The server settings structure to register

## Notes
Registers server settings on server-side and creates server settings interface on client-side.

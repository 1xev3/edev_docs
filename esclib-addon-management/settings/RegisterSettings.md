# RegisterSettings

## Usage example
```lua
addon:RegisterSettings({
    ["General"] = {
        vars = {
            ["enabled"] = {value = true, type = "bool"},
            ["max_players"] = {value = 32, type = "number"}
        }
    }
})
```

## Args:
1. **table** settings - The settings structure to register

## Notes
Registers the initial settings structure for the addon. Can only be called once.

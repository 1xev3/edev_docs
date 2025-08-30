# RegisterSkin

## Usage example
```lua
addon:RegisterSkin("dark_theme", {
    colors = {
        primary = Color(30, 30, 30),
        secondary = Color(60, 60, 60)
    },
    roundsize = 12
})
```

## Args:
1. **string** skin_name - The name of the skin
2. **table** skin_data - The skin configuration data

## Notes
Registers a new skin for the addon. Automatically merges with default skin properties. Only available on client-side.

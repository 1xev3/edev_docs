# SetSkin

## Usage example
```lua
local success = addon:SetSkin("dark_theme")
```

## Args:
1. **string** skin_name - The name of the skin to activate

## Return values:
1. **boolean** - True if skin was set successfully, false otherwise

## Notes
Activates a specific skin for the addon. Triggers skin change hooks. Only available on client-side.

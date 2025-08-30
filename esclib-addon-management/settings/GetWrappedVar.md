# GetWrappedVar

## Usage example
```lua
local value = addon:GetWrappedVar("tab_name", "variable_name")
```

## Args:
1. **string** tab - The settings tab name
2. **string** var - The variable name within the tab

## Return values:
1. **any** - The wrapped variable value

## Notes
Safely retrieves a variable from the settings structure. Returns nil if the tab doesn't exist.

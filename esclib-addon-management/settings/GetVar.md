# GetVar

## Usage example
```lua
local value = addon:GetVar("variable_name")
```

## Args:
1. **string** varid - The variable identifier to retrieve

## Return values:
1. **any** - The variable value (from shared_vars or vars)

## Notes
Retrieves a variable value, checking shared_vars first, then falling back to regular vars.

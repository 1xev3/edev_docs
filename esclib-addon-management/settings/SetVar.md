# SetVar

## Usage example
```lua
addon:SetVar("variable_name", new_value)
```

## Args:
1. **string** varid - The variable identifier to set
2. **any** value - The new value to assign

## Return values:
1. **boolean** - True if successful

## Notes
Sets a variable value, syncs it to settings, and saves the configuration. Triggers automatic synchronization.

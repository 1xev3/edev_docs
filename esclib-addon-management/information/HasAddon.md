# HasAddon

## Usage example
```lua
if esclib:HasAddon("addon_uid") then
    -- Addon exists
end
```

## Args:
1. **string** uid - The unique identifier of the addon

## Return values:
1. **boolean** - True if addon exists, false otherwise

## Notes
Checks if an addon with the specified UID exists in the system.

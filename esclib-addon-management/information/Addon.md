# Addon

## Usage example
```lua
local my_addon = esclib:Addon("my_addon")
my_addon:SetName("My Awesome Addon")
my_addon:SetVersion("1.0.0")
my_addon:SetDescription("A really cool addon")
```

## Args:
1. **string** str_addon - The unique identifier for the addon

## Return values:
1. **table** - The created addon object with metatable

## Notes
Creates a new addon object with default metadata and data structure. If an addon with the same UID already exists, returns the existing one. The UID is automatically converted to lowercase.

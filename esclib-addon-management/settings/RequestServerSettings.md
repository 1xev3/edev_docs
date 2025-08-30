# RequestServerSettings

## Usage example
```lua
addon:RequestServerSettings(function(addon)
    print("Server settings received")
end)
```

## Args:
1. **function** callback - Function to call when server settings are received

## Notes
Requests server settings with an optional callback. Only works for admins. Only available on client-side.

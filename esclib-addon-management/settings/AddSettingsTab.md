# AddSettingsTab

## Usage example
```lua
addon:AddSettingsTab("advanced", "realm_Client", 5, function(addon, panel, callback)
    -- Tab creation logic
end)
```

## Args:
1. **string** uid - Unique identifier for the tab
2. **string** realm - Realm type ("realm_Client" or "realm_Server")
3. **number** sort_order - Sort order for the tab
4. **function** func - Function to create the tab content

## Notes
Adds a custom settings tab to the addon's settings menu. Only available on client-side.

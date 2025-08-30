# GetFilePath

## Usage example
```lua
local file_path = addon:GetFilePath()
```

## Return values:
1. **string** - The addon's file storage path

## Notes
Returns the unique file path for the addon based on UID and server hash. Used for storing settings and data files.

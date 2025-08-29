# KeyFormat

Formats a string by replacing placeholders with values from a replacement table.

## Usage example

```lua
local format_string = "[{rank}] {nickname}:"
local replacements = {rank = "Admin", nickname = "Player123"}
local result = esclib.text:KeyFormat(format_string, replacements)
-- Returns: "[Admin] Player123:"
```

## Args:
1. **string** formatString - The string containing placeholders in {key} format
2. **table** replacements - Table with key-value pairs for replacement

## Return values:
1. **string** result - The formatted string with all placeholders replaced

## Notes
- Placeholders must be in format {key} where key matches a key in replacements table
- Escapes % characters in replacement values to prevent format string issues
- Returns original string if no replacements are found

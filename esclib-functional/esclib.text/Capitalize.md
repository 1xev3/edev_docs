# Capitalize

Capitalizes the first letter of a string.

## Usage example

```lua
local result = esclib.text:Capitalize("hello world")
-- Returns: "Hello world"
```

## Args:
1. **string** str - The string to capitalize

## Return values:
1. **string** result - The string with first letter capitalized

## Notes
- Only capitalizes the first character of the string
- Uses string.gsub with pattern "^%l" to match first lowercase letter
- Leaves all other characters unchanged

# MultilineToString

Converts multiline data back to a single string with newline separators.

## Usage example

```lua
local multiline_data = esclib.text:Multiline("Hello\nWorld", "DermaDefault", 200)
local text_string = esclib.text:MultilineToString(multiline_data)
-- Returns: "Hello\nWorld"
```

## Args:
1. **table** multiline_data - The multiline data table returned by Multiline function

## Return values:
1. **string** text - The concatenated text with newline separators

## Notes
- Joins all lines from multiline_data.lines with "\n" separator
- Useful for converting formatted text back to plain string format

# MatchSplit

Splits a string by pattern matches and returns an array of matched and unmatched segments.

## Usage example

```lua
local str = "<hello>lorem<world> imsulum"
local pattern = "<(.-)>"
local result = esclib.text:MatchSplit(str, pattern)
-- Returns table with matched and unmatched segments
```

## Args:
1. **string** str - The string to split
2. **string** pattern - The pattern to match against

## Return values:
1. **table** result - Array of tables containing:
   - **string** value - The text segment
   - **boolean** matched - True if segment matches pattern (optional)

## Notes
- Returns nil if str or pattern is nil
- If no pattern is found, returns single table with original string
- Each result table contains "value" field, and "matched" field for pattern matches
- Useful for parsing structured text with mixed content

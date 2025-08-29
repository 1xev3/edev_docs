# distance

Calculates the Levenshtein distance between two strings.

## Usage example

```lua
local distance = esclib.text.distance("hello", "helo")
-- Returns: 1 (one character difference)
```

## Args:
1. **string** str1 - First string to compare
2. **string** str2 - Second string to compare

## Return values:
1. **number** distance - The Levenshtein distance between the strings

## Notes
- Levenshtein distance measures the minimum number of single-character edits required to change one string into another
- Uses dynamic programming algorithm for efficient calculation
- Distance of 0 means strings are identical
- Higher distance indicates more differences between strings
- Useful for fuzzy string matching and spell checking

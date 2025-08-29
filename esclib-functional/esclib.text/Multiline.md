# Multiline

Converts text to multiline format with specified width constraints.

## Usage example

```lua
local multiline_data = esclib.text:Multiline("This is a very long text that needs to be wrapped to multiple lines", "DermaDefault", 200, 5)
```

## Args:
1. **string** text - The text to convert to multiline format
2. **string** font - The font to use for text rendering
3. **number** mWidth - Maximum width for each line (optional, defaults to screen width)
4. **number** interval - Spacing between lines (optional, defaults to 2)

## Return values:
1. **table** multiline_data - Table containing:
   - **table** lines - Array of text lines
   - **string** font - The font used
   - **number** spacing - Line spacing (font height + interval)
   - **number** width - Total width of the multiline text
   - **number** height - Total height of the multiline text

## Notes
- Automatically handles word wrapping to prevent words from being cut
- Supports manual line breaks using `\n` in the text
- Uses surface.GetTextSize for accurate text measurements

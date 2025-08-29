# DrawMultiline

Draws multiline text on screen at specified position.

## Usage example

```lua
local multiline_data = esclib.text:Multiline("Hello\nWorld", "DermaDefault", 200)
esclib.text:DrawMultiline(multiline_data, 100, 100, Color(255, 255, 255), TEXT_ALIGN_LEFT, TEXT_ALIGN_TOP)
```

## Args:
1. **table** multiline_data - The multiline data table returned by Multiline function
2. **number** x - X coordinate for text position
3. **number** y - Y coordinate for text position
4. **Color** color - Color of the text
5. **number** alignX - Horizontal alignment (TEXT_ALIGN_LEFT, TEXT_ALIGN_CENTER, TEXT_ALIGN_RIGHT)
6. **number** alignY - Vertical alignment (TEXT_ALIGN_TOP, TEXT_ALIGN_CENTER, TEXT_ALIGN_BOTTOM)

## Notes
- Uses draw.SimpleText for each line of text
- Automatically calculates line spacing based on multiline_data.spacing
- Must be called in a rendering context (HUDPaint, Paint, etc.)

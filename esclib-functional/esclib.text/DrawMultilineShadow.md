# DrawMultilineShadow

Draws multiline text on screen with shadow effect.

## Usage example

```lua
local multiline_data = esclib.text:Multiline("Hello\nWorld", "DermaDefault", 200)
esclib.text:DrawMultilineShadow(multiline_data, 100, 100, Color(255, 255, 255), TEXT_ALIGN_LEFT, TEXT_ALIGN_TOP, 2)
```

## Args:
1. **table** multiline_data - The multiline data table returned by Multiline function
2. **number** x - X coordinate for text position
3. **number** y - Y coordinate for text position
4. **Color** color - Color of the text
5. **number** alignX - Horizontal alignment (TEXT_ALIGN_LEFT, TEXT_ALIGN_CENTER, TEXT_ALIGN_RIGHT)
6. **number** alignY - Vertical alignment (TEXT_ALIGN_TOP, TEXT_ALIGN_CENTER, TEXT_ALIGN_BOTTOM)
7. **number** offsetx - Shadow offset (optional, defaults to 1)

## Notes
- Draws black shadow first, then the colored text on top
- Shadow is drawn with the specified offset in both X and Y directions
- Must be called in a rendering context (HUDPaint, Paint, etc.)

# ShadowText

## Usage example
```lua
esclib.draw:ShadowText("Hello World", "DermaDefault", 100, 100, Color(255, 255, 255), TEXT_ALIGN_LEFT, TEXT_ALIGN_TOP, 2, Color(0, 0, 0))
```

## Args:
1. **string** text - Text to display
2. **string** font - Font name to use
3. **number** px - X position
4. **number** py - Y position
5. **Color** col - Main text color
6. **number** textax - Horizontal text alignment (default: TEXT_ALIGN_LEFT)
7. **number** textay - Vertical text alignment (default: TEXT_ALIGN_TOP)
8. **number** offset - Shadow offset distance (default: 1)
9. **Color** clr - Shadow color (default: esclib.shadow)

## Notes
Draws text with a shadow effect. The shadow is drawn first, then the main text on top for a depth effect.

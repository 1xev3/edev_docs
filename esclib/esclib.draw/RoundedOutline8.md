# RoundedOutline8

## Usage example
```lua
esclib.draw:RoundedOutline8(100, 100, 200, 150, Color(255, 0, 0), true, true, true, true)
```

## Args:
1. **number** x - X position
2. **number** y - Y position
3. **number** w - Width
4. **number** h - Height
5. **Color** clr - Outline color
6. **boolean** lt_corner - Draw left-top corner (default: true)
7. **boolean** rt_corner - Draw right-top corner (default: true)
8. **boolean** rb_corner - Draw right-bottom corner (default: true)
9. **boolean** lb_corner - Draw left-bottom corner (default: true)

## Notes
Draws a rounded outline with 8-pixel radius corners. Uses pre-loaded corner materials for efficient rendering. You can control which corners are drawn by setting the boolean parameters.

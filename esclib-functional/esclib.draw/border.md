# Border

## Usage example
```lua
esclib.draw:Border(100, 100, 200, 150, 2, Color(255, 0, 0), true, true, true, false)
```

## Args:
1. **number** x - X position
2. **number** y - Y position
3. **number** w - Width
4. **number** h - Height
5. **number** thickness - Border thickness
6. **Color** color - Border color
7. **boolean** draw_left - Whether to draw left border (default: true)
8. **boolean** draw_top - Whether to draw top border (default: true)
9. **boolean** draw_right - Whether to draw right border (default: true)
10. **boolean** draw_bottom - Whether to draw bottom border (default: true)

## Notes
Draws a customizable border around a rectangle. You can control which sides of the border are drawn by setting the boolean parameters.

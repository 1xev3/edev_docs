# Material

## Usage example
```lua
esclib.draw:Material(100, 100, 200, 150, Color(255, 255, 255), material)
```

## Args:
1. **number** x - X position
2. **number** y - Y position
3. **number** w - Width
4. **number** h - Height
5. **Color** col - Color tint (default: color_white)
6. **Material** mat - Material to draw

## Notes
Draws a textured rectangle with the specified material. If no material is provided, the function returns early.

# MaterialRotated

## Usage example
```lua
esclib.draw:MaterialRotated(100, 100, 200, 150, 45, Color(255, 255, 255), material)
```

## Args:
1. **number** x - X position
2. **number** y - Y position
3. **number** w - Width
4. **number** h - Height
5. **number** r - Rotation angle in degrees
6. **Color** col - Color tint (default: color_white)
7. **Material** mat - Material to draw

## Notes
Draws a textured rectangle with the specified material rotated around its center. If no material is provided, the function returns early.

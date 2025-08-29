# MaterialCenteredRotated

## Usage example
```lua
esclib.draw:MaterialCenteredRotated(100, 100, 50, 45, Color(255, 255, 255), material)
```

## Args:
1. **number** x - Center X position
2. **number** y - Center Y position
3. **number** r - Radius (half of width/height)
4. **number** rot - Rotation angle in degrees
5. **Color** col - Color tint
6. **Material** mat - Material to draw

## Notes
Draws a square material centered at the specified position and rotated around its center. The material will be r*2 x r*2 pixels in size.

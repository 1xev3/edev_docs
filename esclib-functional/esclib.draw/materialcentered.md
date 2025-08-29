# MaterialCentered

## Usage example
```lua
esclib.draw:MaterialCentered(100, 100, 50, Color(255, 255, 255), material)
```

## Args:
1. **number** x - Center X position
2. **number** y - Center Y position
3. **number** r - Radius (half of width/height)
4. **Color** col - Color tint
5. **Material** mat - Material to draw

## Notes
Draws a square material centered at the specified position. The material will be r*2 x r*2 pixels in size.

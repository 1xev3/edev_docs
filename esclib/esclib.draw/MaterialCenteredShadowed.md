# MaterialCenteredShadowed

## Usage example
```lua
esclib.draw:MaterialCenteredShadowed(100, 100, 50, Color(255, 255, 255), material, 2, Color(0, 0, 0))
```

## Args:
1. **number** x - Center X position
2. **number** y - Center Y position
3. **number** r - Radius (half of width/height)
4. **Color** col - Main material color
5. **Material** mat - Material to draw
6. **number** offset - Shadow offset distance (default: 1)
7. **Color** shadowcolor - Shadow color (default: esclib.shadow)

## Notes
Draws a material with a shadow effect. The shadow is drawn first with an offset, then the main material on top.

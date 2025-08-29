# PolyCircle

## Usage example
```lua
esclib.draw:PolyCircle(100, 100, 50, Color(255, 0, 0), 180)
```

## Args:
1. **number** x - Center X position
2. **number** y - Center Y position
3. **number** r - Radius of the circle
4. **Color** col - Color of the circle
5. **number** v - Number of vertices (default: 360)

## Notes
Draws a filled circle using polygon rendering. Uses GenCircle internally to generate the circle structure.

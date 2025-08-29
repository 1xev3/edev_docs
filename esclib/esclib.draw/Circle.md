# Circle

## Usage example
```lua
esclib.draw:Circle(100, 100, 50, Color(255, 0, 0))
```

## Args:
1. **number** x - Center X position
2. **number** y - Center Y position
3. **number** r - Radius of the circle
4. **Color** col - Color of the circle (default: esclib.white)

## Notes
Draws a circle using a pre-loaded circle material texture. More efficient than polygon-based circles for simple rendering.

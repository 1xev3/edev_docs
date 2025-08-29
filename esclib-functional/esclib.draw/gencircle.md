# GenCircle

## Usage example
```lua
local circle = esclib.draw:GenCircle(100, 100, 50, 180)
```

## Args:
1. **number** x - Center X position
2. **number** y - Center Y position
3. **number** r - Radius of the circle
4. **number** v - Number of vertices/polygons (default: 360)

## Return values:
1. **table** circle - Array of vertex positions with x and y coordinates

## Notes
Generates a circle structure as a series of connected vertices. Higher vertex counts create smoother circles but use more memory.

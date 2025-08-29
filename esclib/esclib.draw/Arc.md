# Arc

## Usage example
```lua
esclib.draw:Arc(100, 100, 50, 2, 0, 180, 32, Color(255, 0, 0), false)
```

## Args:
1. **number** cx - Center X position
2. **number** cy - Center Y position
3. **number** radius - Radius of the arc
4. **number** thickness - Thickness of the arc line
5. **number** startang - Starting angle in degrees
6. **number** endang - Ending angle in degrees
7. **number** roughness - Number of segments (higher = smoother)
8. **Color** color - Color of the arc
9. **boolean** bClockwise - Whether to draw clockwise (default: false)

## Notes
Draws an arc using pre-cached arc data for better performance. The arc is drawn as a series of connected line segments.

# GradientBox

## Usage example
```lua
esclib.draw:GradientBox(100, 100, 200, 150, Color(255, 0, 0), Color(0, 0, 255))
```

## Args:
1. **number** x - X position
2. **number** y - Y position
3. **number** w - Width
4. **number** h - Height
5. **Color** clr1 - Base color
6. **Color** clr2 - Gradient color

## Notes
Draws a box with a gradient effect from left to right. The base color fills the entire box, then the gradient color is applied on top using a rotated gradient material.

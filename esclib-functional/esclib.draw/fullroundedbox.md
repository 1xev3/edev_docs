# FullRoundedBox

## Usage example
```lua
esclib.draw:FullRoundedBox(100, 100, 200, 150, Color(255, 0, 0))
```

## Args:
1. **number** x - X position
2. **number** y - Y position
3. **number** w - Width
4. **number** h - Height
5. **Color** col - Color

## Notes
Draws a fully rounded rectangle using new half-circle materials for the ends and a rounded box for the middle section. More efficient than the deprecated FullRoundedCircle function.

# BlurRect

## Usage example
```lua
esclib.draw:BlurRect(100, 100, 200, 150, 4)
```

## Args:
1. **number** x - X position of blur area
2. **number** y - Y position of blur area
3. **number** w - Width of blur area
4. **number** h - Height of blur area
5. **number** count - Number of blur passes (default: 2)

## Notes
Applies a blur effect to a specific rectangular area using scissor rect for clipping. More efficient than full-screen blur when only a small area needs blurring.

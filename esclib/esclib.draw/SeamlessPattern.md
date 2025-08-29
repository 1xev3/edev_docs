# SeamlessPattern

## Usage example
```lua
esclib.draw:SeamlessPattern(100, 100, 200, 150, 64, 64, Color(255, 255, 255), material, 32, 16)
```

## Args:
1. **number** x - X position
2. **number** y - Y position
3. **number** w - Width of pattern area
4. **number** h - Height of pattern area
5. **number** tex_w - Texture width
6. **number** tex_h - Texture height
7. **Color** col - Color tint
8. **Material** mat - Material to use as pattern
9. **number** offset_x - X offset for seamless tiling (default: 0)
10. **number** offset_y - Y offset for seamless tiling (default: 0)

## Notes
Draws a seamless repeating pattern using UV mapping. Useful for creating tiled textures that repeat without visible seams.

# GradientText

## Usage example
```lua
local gradient = esclib.draw:GradientText("Hello World", "DermaDefault", Color(255, 0, 0), Color(0, 0, 255))
gradient:Draw(100, 100, TEXT_ALIGN_CENTER, TEXT_ALIGN_CENTER, true)
```

## Args:
1. **string** text - Text to create gradient for
2. **string** font - Font name
3. **Color** col1 - Starting color
4. **Color** col2 - Ending color

## Return values:
1. **table** result - Gradient text object with Draw method and info

## Notes
Creates a gradient text structure that interpolates between two colors. The returned object has a Draw method that renders the gradient text. Each character gets its own interpolated color.

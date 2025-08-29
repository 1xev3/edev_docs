# Blur

## Usage example
```lua
esclib.draw:Blur(panel, 3, 5)
```

## Args:
1. **Panel** pnl - Panel to blur behind
2. **number** cycles - Number of blur passes (default: 1)
3. **number** amount - Blur intensity (default: 3)

## Notes
Applies a screen blur effect behind the specified panel. This function is meant to be used with masking. The blur effect covers the entire screen area.

# SurfaceArc

## Usage example
```lua
esclib.draw:SurfaceArc(arc_data, 180)
```

## Args:
1. **table** arc - Pre-generated arc data structure
2. **number** todraw - Maximum number of arc segments to draw (default: math.huge)

## Notes
Renders a pre-generated arc structure using polygon drawing. Used internally by the Arc function. The arc data should be generated using esclib.util.PrecacheArc.

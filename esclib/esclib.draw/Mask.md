# Mask

## Usage example
```lua
esclib.draw:Mask(
    function() 
        -- Mask drawing function
        surface.DrawRect(0, 0, 100, 100)
    end,
    function()
        -- Content drawing function
        surface.DrawTexturedRect(0, 0, 100, 100, material)
    end,
    false, -- inverse
    1      -- reference
)
```

## Args:
1. **function** func - Function that draws the mask
2. **function** drawfunc - Function that draws the content
3. **boolean** inverse - Whether to invert the mask (default: false)
4. **number** reference - Stencil reference value (default: 1)

## Notes
Uses OpenGL stencil buffer to create masking effects. The first function creates the mask, the second function draws content only where the mask exists.

---
icon: knife-kitchen
---

# esclib.draw:Mask

```lua
esclib.draw:Mask(
    draw_mask: function,
    draw_content: function,
    inverse: boolean, 
    reference: boolean, --mask parameters
    self, w, h  --passthrough parameters (for example)
)
```

### Usage example

```lua
local function draw_mask(w,h)
    if not self.poly then
        self.poly = esclib.util:PrecacheRoundedPoly(0, 0, w, h, 16, 3)
    end
    draw.NoTexture();
    surface.SetDrawColor( color_white )
    surface.DrawPoly( self.poly )
end

local function draw_paint(w,h)
    draw.RoundedBox(0,0,0,w,h,color_white)
end

function pnl:Paint(w,h)
    esclib.draw:Mask(draw_mask, draw_paint, false,nil, w,h)
end
```

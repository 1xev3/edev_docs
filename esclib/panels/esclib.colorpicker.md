---
description: >-
  A custom color picker panel for Garry's Mod that provides HSV color selection,
  RGB value inputs, alpha channel support, and color palette functionality.
---

# esclib.colorpicker

### Usage example

```lua
local colorPicker = vgui.Create("esclib.colorpicker")
colorPicker:SetSize(285, 175)
colorPicker:SetColor(Color(255, 0, 0, 255))
colorPicker:SetLabel("Choose Color")
colorPicker:SetPalette(true)
colorPicker:SetAlphaBar(true)
colorPicker:SetWangs(true)

-- Set ConVars for automatic value binding
colorPicker:SetConVarR("my_color_r")
colorPicker:SetConVarG("my_color_g") 
colorPicker:SetConVarB("my_color_b")
colorPicker:SetConVarA("my_color_a")

-- Handle color changes
function colorPicker:ValueChanged(color)
    print("Color changed to:", color.r, color.g, color.b, color.a)
end
```

### Methods

#### Getter Methods

| Name          | Description                                                  |
| ------------- | ------------------------------------------------------------ |
| GetColor()    | Returns the current color as a Color object                  |
| GetVector()   | Returns the current color as a normalized Vector (0-1 range) |
| GetConVarR()  | Returns the red channel ConVar name                          |
| GetConVarG()  | Returns the green channel ConVar name                        |
| GetConVarB()  | Returns the blue channel ConVar name                         |
| GetConVarA()  | Returns the alpha channel ConVar name                        |
| GetPalette()  | Returns whether the color palette is enabled                 |
| GetAlphaBar() | Returns whether the alpha bar is visible                     |
| GetWangs()    | Returns whether the number input panels are visible          |

#### Setter Methods

| Name                 | Description                                                          |
| -------------------- | -------------------------------------------------------------------- |
| SetColor(color)      | Sets the current color and updates all components                    |
| SetVector(vec)       | Sets color from a normalized Vector (0-1 range)                      |
| SetConVarR(cvar)     | Sets the ConVar name for red channel binding                         |
| SetConVarG(cvar)     | Sets the ConVar name for green channel binding                       |
| SetConVarB(cvar)     | Sets the ConVar name for blue channel binding                        |
| SetConVarA(cvar)     | Sets the ConVar name for alpha channel binding and enables alpha bar |
| SetPalette(enabled)  | Shows/hides the color palette at the bottom                          |
| SetAlphaBar(enabled) | Shows/hides the alpha channel bar and input                          |
| SetWangs(enabled)    | Shows/hides the RGB number input panels                              |
| SetLabel(text)       | Sets the label text above the color picker                           |
| SetBaseColor(color)  | Sets the base color for HSV selection                                |

#### Event Methods

| Name                | Description                                                     |
| ------------------- | --------------------------------------------------------------- |
| ValueChanged(color) | Called when the color value changes (override to handle events) |
| UpdateColor(color)  | Updates all component                                           |

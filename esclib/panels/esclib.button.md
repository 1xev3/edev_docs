---
description: >-
  A customizable button panel for esclib with support for icons, text, and
  various styling options.
---

# esclib.button

### Usage example

```lua
local button = vgui.Create("esclib.button")
button:SetSize(200, 50)
button:SetButtonText("Click me")
button:SetIcon(Material("icon16/star.png"))
button:SetIconSize(0.8)
button:SetBorderRadius(10)
button:SetBackgroundColor(Color(50, 50, 50))
button:SetBackgroundHoverColor(Color(70, 70, 70))
button:SetTextColor(Color(255, 255, 255))
button:SetTextHoverColor(Color(200, 200, 200))
button:SetEnabled(true)
button:SetTextAlignX(TEXT_ALIGN_CENTER)
button:SetTextAlignY(TEXT_ALIGN_CENTER)
button:SetTextYOffset(0)
button:SetIconOffset(8)
button:SetDrawTextShadow(true)
button:SetDrawIconShadow(false)
button:StretchWidth(20)
```

### Methods

#### Getter Methods

| Name                         | Description                                    |
| ---------------------------- | ---------------------------------------------- |
| GetBorderRadius()            | Get the border radius of the button            |
| GetButtonText()              | Get the text displayed on the button           |
| GetTextAlignX()              | Get the horizontal text alignment              |
| GetTextAlignY()              | Get the vertical text alignment                |
| GetIconSize()                | Get the icon size multiplier                   |
| GetIconOffset()              | Get the offset between icon and text           |
| GetTextYOffset()             | Get the vertical offset for text               |
| GetEnabled()                 | Check if the button is enabled                 |
| GetDrawTextShadow()          | Check if text shadow is enabled                |
| GetDrawIconShadow()          | Check if icon shadow is enabled                |
| GetIcon()                    | Get the icon material                          |
| GetBackgroundColor()         | Get the main background color                  |
| GetBackgroundHoverColor()    | Get the background color on hover              |
| GetBackgroundDisabledColor() | Get the background color when disabled         |
| GetBackgroundColor2()        | Get the secondary background color             |
| GetBackgroundHoverColor2()   | Get the secondary background color on hover    |
| GetTextColor()               | Get the text color                             |
| GetTextHoverColor()          | Get the text color on hover                    |
| GetIconColor()               | Get the icon color                             |
| GetIconHoverColor()          | Get the icon color on hover                    |
| GetText()                    | Get the button text (alias for GetButtonText)  |
| IsDown()                     | Check if the button is currently pressed       |
| IsEnabled()                  | Check if the button is enabled                 |
| IsHovered()                  | Check if the mouse is hovering over the button |

#### Setter Methods

| Name                              | Description                                                                                    |
| --------------------------------- | ---------------------------------------------------------------------------------------------- |
| SetBorderRadius(radius)           | Set the border radius of the button                                                            |
| SetButtonText(text)               | Set the text displayed on the button                                                           |
| SetTextAlignX(alignment)          | Set the horizontal text alignment (TEXT\_ALIGN\_LEFT, TEXT\_ALIGN\_CENTER, TEXT\_ALIGN\_RIGHT) |
| SetTextAlignY(alignment)          | Set the vertical text alignment (TEXT\_ALIGN\_TOP, TEXT\_ALIGN\_CENTER, TEXT\_ALIGN\_BOTTOM)   |
| SetIconSize(size)                 | Set the icon size multiplier (0.0 to 1.0)                                                      |
| SetIconOffset(offset)             | Set the offset between icon and text                                                           |
| SetTextYOffset(offset)            | Set the vertical offset for text                                                               |
| SetEnabled(enabled)               | Enable or disable the button                                                                   |
| SetDrawTextShadow(enabled)        | Enable or disable text shadow                                                                  |
| SetDrawIconShadow(enabled)        | Enable or disable icon shadow                                                                  |
| SetIcon(material)                 | Set the icon material                                                                          |
| SetBackgroundColor(color)         | Set the main background color                                                                  |
| SetBackgroundHoverColor(color)    | Set the background color on hover                                                              |
| SetBackgroundDisabledColor(color) | Set the background color when disabled                                                         |
| SetBackgroundColor2(color)        | Set the secondary background color                                                             |
| SetBackgroundHoverColor2(color)   | Set the secondary background color on hover                                                    |
| SetTextColor(color)               | Set the text color                                                                             |
| SetTextHoverColor(color)          | Set the text color on hover                                                                    |
| SetIconColor(color)               | Set the icon color                                                                             |
| SetIconHoverColor(color)          | Set the icon color on hover                                                                    |
| SetText(text)                     | Set the button text (alias for SetButtonText)                                                  |
| StretchWidth(additional\_width)   | Automatically resize the button width based on text and icon                                   |

#### Override Methods

| Name                  | Description                                                                    |
| --------------------- | ------------------------------------------------------------------------------ |
| BeforePaint(w, h)     | Called before painting, can be overridden for custom pre-paint logic           |
| PaintBackground(w, h) | Called to paint the button background, can be overridden for custom background |

***

## esclib.glow\_button

A button panel with glow effects that extends esclib.button functionality.

### Usage example

```lua
local glowButton = vgui.Create("esclib.glow_button")
glowButton:SetSize(200, 50)
glowButton:SetButtonText("Glow Button")
glowButton:SetGlowMode("radial")
glowButton:SetGlowColor(Color(255, 0, 0, 100))
glowButton:SetGlowSizeX(0.5)
glowButton:SetGlowSizeY(0.7)
```

### Methods

#### Getter Methods

| Name           | Description                                        |
| -------------- | -------------------------------------------------- |
| GetGlowSizeX() | Get the horizontal glow size multiplier            |
| GetGlowSizeY() | Get the vertical glow size multiplier              |
| GetGlowColor() | Get the glow color                                 |
| GetGlowMode()  | Get the glow mode ("radial", "mouse", or "always") |

#### Setter Methods

| Name                | Description                                        |
| ------------------- | -------------------------------------------------- |
| SetGlowSizeX(size)  | Set the horizontal glow size multiplier            |
| SetGlowSizeY(size)  | Set the vertical glow size multiplier              |
| SetGlowColor(color) | Set the glow color                                 |
| SetGlowMode(mode)   | Set the glow mode ("radial", "mouse", or "always") |

#### Glow Modes

* **"radial"**: Glow effect radiates from the center of the button
* **"mouse"**: Glow effect follows the mouse cursor position
* **"always"**: Glow effect is always visible

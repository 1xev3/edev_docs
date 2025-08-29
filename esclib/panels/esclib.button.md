# esclib.button

### esclib.button

A customizable button panel for esclib with support for icons, text, and various styling options.

#### Methods:

**Core Methods:**

* `SetBorderRadius(radius)` - Sets the border radius of the button
* `SetButtonText(text)` - Sets the button text
* `SetTextAlignX(alignment)` - Sets horizontal text alignment (TEXT\_ALIGN\_LEFT, TEXT\_ALIGN\_CENTER, TEXT\_ALIGN\_RIGHT)
* `SetTextAlignY(alignment)` - Sets vertical text alignment
* `SetIconSize(size)` - Sets icon size multiplier (0.5 \* height \* size)
* `SetIconOffset(offset)` - Sets spacing between icon and text
* `SetTextYOffset(offset)` - Sets vertical offset for text
* `SetEnabled(enabled)` - Enables/disables the button
* `SetDrawTextShadow(enabled)` - Enables text shadow
* `SetDrawIconShadow(enabled)` - Enables icon shadow
* `SetIcon(material)` - Sets the button icon material
* `GetIcon()` - Returns the current icon material

**Color Methods:**

* `SetBackgroundColor(color)` - Sets main background color
* `SetBackgroundHoverColor(color)` - Sets background color on hover
* `SetBackgroundDisabledColor(color)` - Sets background color when disabled
* `SetBackgroundColor2(color)` - Sets secondary background color
* `SetBackgroundHoverColor2(color)` - Sets secondary background color on hover
* `SetTextColor(color)` - Sets text color
* `SetTextHoverColor(color)` - Sets text color on hover
* `SetIconColor(color)` - Sets icon color
* `SetIconHoverColor(color)` - Sets icon color on hover

**Utility Methods:**

* `IsDown()` - Returns true if button is pressed
* `IsEnabled()` - Returns true if button is enabled
* `StretchWidth(additional_width)` - Automatically adjusts button width to fit content
* `BeforePaint(w, h)` - Override function called before painting
* `PaintBackground(w, h)` - Override function for custom background painting

#### Usage Example:

```lua
local button = vgui.Create("esclib.button")
button:SetSize(200, 40)
button:SetButtonText("Click Me")
button:SetIcon(Material("icon16/star.png"))
button:SetBackgroundColor(Color(50, 50, 50))
button:SetBackgroundHoverColor(Color(70, 70, 70))
button:SetTextColor(Color(255, 255, 255))
button:SetBorderRadius(8)
button:SetIconSize(0.8)
button:SetIconOffset(10)
```

### esclib.glow\_button

A button with glow effect capabilities, inherits from esclib.button.

#### Methods:

**Glow Methods:**

* `SetGlowSizeX(size)` - Sets horizontal glow size multiplier
* `SetGlowSizeY(size)` - Sets vertical glow size multiplier
* `SetGlowColor(color)` - Sets glow color
* `SetGlowMode(mode)` - Sets glow mode ("radial", "mouse", "always")

#### Usage Example:

```lua
local glowButton = vgui.Create("esclib.glow_button")
glowButton:SetSize(200, 40)
glowButton:SetButtonText("Glow Button")
glowButton:SetGlowMode("radial")
glowButton:SetGlowColor(Color(255, 0, 0, 100))
glowButton:SetGlowSizeX(0.5)
glowButton:SetGlowSizeY(0.7)
```

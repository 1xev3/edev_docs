---
description: >-
  A custom VGUI panel that provides flexible icon-based layout management with
  automatic positioning and sizing capabilities.
---

# esclib.iconlayout

## esclib.iconlayout

### Methods:

#### Layout Control

* **SetStretchHeight(bStretch)** - Enables/disables automatic height adjustment based on content
* **SetStretchWidth(bStretch)** - Enables/disables automatic width adjustment based on content
* **SetBorder(border)** - Sets all border values to the same value
* **SetPadding(pLeft, pTop, pRight, pBottom)** - Sets individual border/padding values
* **GetBorder()** - Returns the left border value
* **SetSpaceX(x)** - Sets horizontal spacing between panels
* **GetSpaceX()** - Returns current horizontal spacing
* **SetSpaceY(y)** - Sets vertical spacing between panels
* **GetRowSizeFor(rows)** - Calculates row height for specified number of rows
* **GetColumnSizeFor(cols)** - Calculates column width for specified number of columns

#### Content Management

* **Add(pnl)** - Adds a panel to the layout and automatically positions it
* **RemoveItem(item)** - Removes a specific panel from the layout
* **Clear()** - Removes all panels from the layout
* **Layout()** - Performs layout calculation and positioning
* **CalculateSize()** - Recalculates size without repositioning elements
* **PerformLayout(w, h)** - Override method that calls Layout()

#### Configuration

* **SetMaxHeight(height)** - Sets maximum height constraint (0 = no limit)
* **SetMinHeight(height)** - Sets minimum height constraint (0 = no limit)
* **SetIgnoreHiddenChildren(ignore)** - Controls whether hidden children affect layout
* **SetZPosSorting(enabled)** - Enables/disables Z-position based sorting

#### Callbacks

* **OnLayout()** - Override method called when layout is completed

### Usage Example:

```lua
local layout = vgui.Create("esclib.iconlayout")
layout:SetSize(400, 0)
layout:SetStretchHeight(true)
layout:SetBorder(10)
layout:SetSpaceX(5)
layout:SetSpaceY(5)

-- Add panels
local button1 = vgui.Create("DButton")
button1:SetSize(80, 80)
layout:Add(button1)

local button2 = vgui.Create("DButton")
button2:SetSize(120, 60)
layout:Add(button2)
```

### Key Features:

* Automatic wrapping to new rows when content exceeds width
* Configurable spacing and borders
* Auto-sizing capabilities
* Hidden child management
* Z-position sorting support
* Height constraints with min/max limits

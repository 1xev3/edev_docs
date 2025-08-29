---
description: >-
  A custom VGUI panel that provides flexible icon-based layout management with
  automatic positioning and sizing of child panels.
---

# esclib.iconlayout

### Usage example

```lua
local layout = vgui.Create("esclib.iconlayout", parent)
layout:SetSize(600, 400)
layout:SetSpacing(10, 10)
layout:SetBorder(10, 10, 10, 10)
layout:SetStretchHeight(true)
layout:SetStretchWidth(true)

-- Add child panels
local button = vgui.Create("DButton")
button:SetSize(100, 50)
layout:Add(button)

-- Layout will automatically arrange children and resize itself
```

### Methods

#### Layout Management

| Name                | Description                                                       |
| ------------------- | ----------------------------------------------------------------- |
| Layout()            | Arranges all child panels in a grid layout and updates panel size |
| CalculateSize()     | Recalculates panel size without repositioning child elements      |
| PerformLayout(w, h) | Override that calls Layout() when panel is resized                |

#### Child Panel Management

| Name             | Description                                                |
| ---------------- | ---------------------------------------------------------- |
| Add(pnl)         | Adds a panel to the layout and immediately performs layout |
| RemoveItem(item) | Removes a specific child panel from the layout             |
| Clear()          | Removes all child panels and clears the layout             |

#### Spacing and Borders

| Name                                     | Description                            |
| ---------------------------------------- | -------------------------------------- |
| SetSpaceX(x)                             | Sets horizontal spacing between panels |
| SetSpaceY(y)                             | Sets vertical spacing between panels   |
| SetBorder(border)                        | Sets all borders to the same value     |
| SetPadding(pLeft, pTop, pRight, pBottom) | Sets individual border values          |

#### Auto-sizing

| Name                       | Description                                  |
| -------------------------- | -------------------------------------------- |
| SetStretchHeight(bStretch) | Enables/disables automatic height adjustment |
| SetStretchWidth(bStretch)  | Enables/disables automatic width adjustment  |

#### Utility

| Name                   | Description                                                 |
| ---------------------- | ----------------------------------------------------------- |
| GetColumnSizeFor(cols) | Calculates optimal column width for given number of columns |
| GetRowSizeFor(rows)    | Calculates optimal row height for given number of rows      |
| OnLayout()             | Override method called after layout is completed            |

### Getter Methods

| Name                      | Description                                 |
| ------------------------- | ------------------------------------------- |
| GetBorder()               | Returns the left border value               |
| GetSpaceX()               | Returns horizontal spacing value            |
| GetSpaceY()               | Returns vertical spacing value              |
| GetBorderLeft()           | Returns left border value                   |
| GetBorderTop()            | Returns top border value                    |
| GetBorderRight()          | Returns right border value                  |
| GetBorderBottom()         | Returns bottom border value                 |
| GetMaxHeight()            | Returns maximum height constraint           |
| GetMinHeight()            | Returns minimum height constraint           |
| GetIgnoreHiddenChildren() | Returns whether hidden children are ignored |
| GetZPosSorting()          | Returns whether Z-pos sorting is enabled    |

### Setter Methods

| Name                           | Description                                              |
| ------------------------------ | -------------------------------------------------------- |
| SetBorderLeft(value)           | Sets left border value                                   |
| SetBorderTop(value)            | Sets top border value                                    |
| SetBorderRight(value)          | Sets right border value                                  |
| SetBorderBottom(value)         | Sets bottom border value                                 |
| SetMaxHeight(value)            | Sets maximum height constraint (0 = no limit)            |
| SetMinHeight(value)            | Sets minimum height constraint (0 = no limit)            |
| SetIgnoreHiddenChildren(value) | Sets whether hidden children should be ignored in layout |
| SetZPosSorting(value)          | Sets whether children should be sorted by Z-pos          |

### Features

* **Automatic Layout**: Child panels are automatically arranged in a grid pattern
* **Flexible Sizing**: Supports automatic width/height adjustment based on content
* **Border Control**: Configurable borders and padding on all sides
* **Spacing Control**: Independent horizontal and vertical spacing between panels
* **Hidden Children**: Option to ignore hidden child panels in layout calculations
* **Z-Position Sorting**: Optional sorting of children by Z-pos for proper layering
* **Height Constraints**: Minimum and maximum height limits for auto-sizing
* **Column/Row Utilities**: Helper methods for calculating optimal sizes for grid layouts

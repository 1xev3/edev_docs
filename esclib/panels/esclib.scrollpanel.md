---
description: >-
  A custom scrollable panel that extends DPanel with enhanced scrolling
  functionality and custom scrollbar integration.
---

# esclib.scrollpanel

### Usage example

```lua
local scrollPanel = vgui.Create("esclib.scrollpanel")
scrollPanel:SetSize(300, 400)
scrollPanel:SetPadding(10)
scrollPanel:SetScrollSpeed(15)

-- Add content to the panel
local button = vgui.Create("DButton", scrollPanel)
button:SetText("Example Button")
button:SetSize(200, 30)

-- Scroll to specific child
scrollPanel:ScrollToChild(button, true)

-- Scroll to bottom
scrollPanel:ScrollToBottom()

-- Get/Set scroll position
local currentScroll = scrollPanel:GetScroll()
scrollPanel:SetScroll(50)
```

### Methods

#### Content Management

| Name             | Description                            |
| ---------------- | -------------------------------------- |
| AddItem(pnl)     | Adds a panel as a child to the canvas  |
| Clear()          | Removes all children from the canvas   |
| SizeToContents() | Resizes the panel to match canvas size |

#### Scrolling

| Name                          | Description                              |
| ----------------------------- | ---------------------------------------- |
| ScrollToBottom()              | Scrolls to the bottom of the content     |
| ScrollToChild(panel, animate) | Scrolls to make a specific child visible |
| OnMouseWheeled(dlta)          | Handles mouse wheel scrolling            |
| OnVScroll(iOffset)            | Updates canvas position when scrolling   |

#### Layout & Sizing

| Name                    | Description                              |
| ----------------------- | ---------------------------------------- |
| Rebuild()               | Recalculates canvas size and positioning |
| PerformLayout()         | Performs layout calculations             |
| PerformLayoutInternal() | Internal layout logic                    |
| InnerWidth()            | Returns the width of the canvas          |

#### Canvas & Scrollbar Access

| Name        | Description                    |
| ----------- | ------------------------------ |
| GetCanvas() | Returns the canvas panel       |
| GetVBar()   | Returns the vertical scrollbar |

#### Getters

| Name             | Description                     |
| ---------------- | ------------------------------- |
| GetPadding()     | Returns the padding value       |
| GetScrollSpeed() | Returns the scroll speed        |
| GetCanvas()      | Returns the canvas panel        |
| GetScroll()      | Returns current scroll position |
| GetVBar()        | Returns the vertical scrollbar  |

#### Setters

| Name                  | Description                                 |
| --------------------- | ------------------------------------------- |
| SetPadding(value)     | Sets the padding around content             |
| SetScrollSpeed(value) | Sets the scroll speed and updates scrollbar |
| SetScroll(scroll)     | Sets the scroll position                    |

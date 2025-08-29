---
description: >-
  A customizable frame panel with gradient effects, draggable functionality, and
  modern styling.
---

# esclib.frame

### Usage example

```lua
local frame = vgui.Create("esclib.frame")
frame:SetSize(400, 300)
frame:SetTitle("My Window", Color(255, 255, 255), "esclib_22_500", TEXT_ALIGN_LEFT, TEXT_ALIGN_CENTER)
frame:SetBackgroundColor(Color(13, 13, 13))
frame:SetRoundSize(16)
frame:SetDraggable(true)
frame:SetSizable(false)
frame:SetScreenLock(false)
frame:EnableCloseButton(true)
frame:SetIcon(material)
frame:SetGradientColor(Color(255, 0, 0, 255))
frame:SetTargetGradientColor(Color(0, 255, 0, 255))
frame:Close()
```

### Methods

#### Getter Methods

| Name                     | Description                                          |
| ------------------------ | ---------------------------------------------------- |
| GetDraggable()           | Returns whether the frame is draggable               |
| GetScreenLock()          | Returns whether the frame is locked to screen bounds |
| GetSizable()             | Returns whether the frame can be resized             |
| GetColorThink()          | Returns whether color animation is enabled           |
| GetAutoRestoreColor()    | Returns whether colors auto-restore                  |
| GetMinWidth()            | Returns minimum width of the frame                   |
| GetMinHeight()           | Returns minimum height of the frame                  |
| GetGainFraction()        | Returns color gain animation speed                   |
| GetRestoreFraction()     | Returns color restore animation speed                |
| GetGradientColor()       | Returns current gradient color                       |
| GetTargetGradientColor() | Returns target gradient color                        |
| GetColor()               | Returns background color                             |
| GetBorderColor()         | Returns border color                                 |
| GetTitle()               | Returns frame title text                             |
| GetTitleColor()          | Returns title text color                             |
| GetContent()             | Returns content panel                                |
| GetTitlePanel()          | Returns title panel                                  |

#### Setter Methods

| Name                                         | Description                             |
| -------------------------------------------- | --------------------------------------- |
| SetDraggable(bool)                           | Enable/disable frame dragging           |
| SetScreenLock(bool)                          | Lock frame to screen boundaries         |
| SetSizable(bool)                             | Enable/disable frame resizing           |
| SetColorThink(bool)                          | Enable/disable color animation          |
| SetAutoRestoreColor(bool)                    | Enable/disable auto color restoration   |
| SetMinWidth(number)                          | Set minimum frame width                 |
| SetMinHeight(number)                         | Set minimum frame height                |
| SetGainFraction(number)                      | Set color gain animation speed          |
| SetRestoreFraction(number)                   | Set color restore animation speed       |
| SetGradientColor(color)                      | Set current gradient color              |
| SetTargetGradientColor(color)                | Set target gradient color for animation |
| SetBackgroundColor(color)                    | Set frame background color              |
| SetBorderColor(color)                        | Set frame border color                  |
| SetTitle(title, color, font, alignx, aligny) | Set title with optional styling         |
| SetTitleColor(color)                         | Set title text color                    |
| SetIcon(material)                            | Set title icon                          |
| SetRoundSize(number)                         | Set corner roundness                    |

#### Control Methods

| Name                    | Description                            |
| ----------------------- | -------------------------------------- |
| EnableCloseButton(bool) | Show/hide close button                 |
| Close(callback)         | Close the frame with optional callback |
| OnClose(callback)       | Override close behavior                |
| PerformLayout()         | Recalculate layout and positioning     |

#### Event Methods

| Name                      | Description                  |
| ------------------------- | ---------------------------- |
| OnDragging(newx, newy)    | Called during drag operation |
| OnStartDragging(x, y)     | Called when drag starts      |
| OnEndDragging(newx, newy) | Called when drag ends        |
| OnPress()                 | Called on mouse press        |
| OnUnpress()               | Called on mouse release      |

#### Internal Methods

| Name              | Description                              |
| ----------------- | ---------------------------------------- |
| Init()            | Initialize the frame panel               |
| Think()           | Handle animations and mouse interactions |
| Paint(w, h)       | Render the frame with gradient effects   |
| PaintTitle(w, h)  | Render the title bar                     |
| PaintBG(w, h)     | Render the background                    |
| OnMousePressed()  | Handle mouse press events                |
| OnMouseReleased() | Handle mouse release events              |

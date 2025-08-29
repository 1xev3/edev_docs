---
description: >-
  A draggable and resizable base panel for ESCLib UI system. This panel provides
  drag functionality with customizable drag areas and resize capabilities.
---

# esclib.dragbase

### Usage example

```lua
local panel = vgui.Create("esclib.dragbase")
panel:SetSize(400, 300)
panel:SetPos(100, 100)
panel:SetDraggable(true)
panel:SetSizable(true)
panel:SetScreenLock(true)
panel:SetMinWidth(200)
panel:SetMinHeight(150)
panel:SetDragArea(0, 0, 400, 30) -- Set custom drag area

-- Override paint method
function panel:Paint(w, h)
    surface.SetDrawColor(50, 50, 50, 255)
    surface.DrawRect(0, 0, w, h)
end
```

### Methods

#### Getters

| Name            | Description                                          |
| --------------- | ---------------------------------------------------- |
| GetDraggable()  | Returns whether the panel is draggable               |
| GetScreenLock() | Returns whether the panel is locked to screen bounds |
| GetSizable()    | Returns whether the panel can be resized             |
| GetMinWidth()   | Returns the minimum width of the panel               |
| GetMinHeight()  | Returns the minimum height of the panel              |

#### Setters

| Name                 | Description                                              |
| -------------------- | -------------------------------------------------------- |
| SetDraggable(bool)   | Sets whether the panel is draggable                      |
| SetScreenLock(bool)  | Sets whether the panel should be locked to screen bounds |
| SetSizable(bool)     | Sets whether the panel can be resized                    |
| SetMinWidth(number)  | Sets the minimum width of the panel                      |
| SetMinHeight(number) | Sets the minimum height of the panel                     |

#### Core Methods

| Name                    | Description                                                       |
| ----------------------- | ----------------------------------------------------------------- |
| SetDragArea(x, y, w, h) | Sets the custom drag area within the panel                        |
| UpdateDragArea()        | Updates the drag area to match panel dimensions                   |
| IsMouseInDragArea()     | Returns true if mouse is within the drag area                     |
| IsMouseInSizeArea()     | Returns true if mouse is in the resize area (bottom-right corner) |

#### Event Handlers

| Name                      | Description                               |
| ------------------------- | ----------------------------------------- |
| OnDragging(newx, newy)    | Called while dragging the panel           |
| OnSizing(neww, newh)      | Called while resizing the panel           |
| OnStartDragging(x, y)     | Called when dragging starts               |
| OnEndDragging(newx, newy) | Called when dragging ends                 |
| OnEndSizing(neww, newh)   | Called when resizing ends                 |
| OnPress()                 | Called when mouse is pressed              |
| OnUnpress()               | Called when mouse is released             |
| Paint(w, h)               | Called to paint the panel (override this) |

#### Internal Methods

| Name              | Description                                |
| ----------------- | ------------------------------------------ |
| OnMousePressed()  | Handles mouse press events for drag/resize |
| OnMouseReleased() | Handles mouse release events               |
| Think()           | Main update loop for drag/resize logic     |

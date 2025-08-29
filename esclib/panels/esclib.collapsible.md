# esclib.collapsible

## esclib.collapsible

A collapsible panel component that provides an expandable/collapsible interface with a header bar and content area.

### Usage example

```lua
local collapsible = vgui.Create("esclib.collapsible")
collapsible:SetSize(300, 200)
collapsible:SetPos(10, 10)

-- Add content to the collapsible
local content = collapsible:GetContent()
local button = content:Add("DButton")
button:SetText("Click me")

-- Control the collapsible state
collapsible:Open()  -- Expand the panel
collapsible:Close() -- Collapse the panel

-- Check if panel is opened
if collapsible:IsOpened() then
    print("Panel is expanded")
end

-- Set animation state
collapsible:SetAnimate(true)

-- Override callbacks
function collapsible:OnOpen()
    print("Panel opened")
end

function collapsible:OnClose()
    print("Panel closed")
end
```

### Methods

#### Getter Methods

| Name         | Description                                     |
| ------------ | ----------------------------------------------- |
| GetAnimate() | Returns whether the panel uses animations       |
| GetHeader()  | Returns the header button panel                 |
| GetContent() | Returns the content container panel             |
| IsOpened()   | Returns true if the panel is currently expanded |

#### Setter Methods

| Name                | Description                                  |
| ------------------- | -------------------------------------------- |
| SetAnimate(animate) | Sets whether the panel should use animations |

#### Control Methods

| Name    | Description                                       |
| ------- | ------------------------------------------------- |
| Open()  | Expands the collapsible panel and shows content   |
| Close() | Collapses the collapsible panel and hides content |

#### Override Methods

| Name           | Description                                                         |
| -------------- | ------------------------------------------------------------------- |
| OnOpen()       | Called when the panel is opened (can be overridden)                 |
| OnClose()      | Called when the panel is closed (can be overridden)                 |
| OnRemove()     | Called when the panel is removed (can be overridden)                |
| AnimTick(frac) | Called during animation with animation fraction (can be overridden) |
| Paint(w, h)    | Custom painting function (can be overridden)                        |

#### Layout Methods

| Name            | Description                               |
| --------------- | ----------------------------------------- |
| PerformSize()   | Recalculates and updates panel dimensions |
| PerformLayout() | Triggers layout recalculation             |

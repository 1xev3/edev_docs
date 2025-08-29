---
description: >-
  A tabbed interface panel that provides a navigation bar with tabs and content
  area. Supports smooth animations between tab transitions and customizable
  styling.
---

# esclib.combolist

### Usage example

```lua
local combolist = vgui.Create("esclib.combolist")
combolist:SetSize(400, 300)
combolist:SetPos(10, 10)

-- Add tabs with content
combolist:AddTab("General", function(parent)
    local label = parent:Add("DLabel")
    label:SetText("General settings content")
    label:SizeToContents()
end)

combolist:AddTab("Advanced", function(parent)
    local button = parent:Add("DButton")
    button:SetText("Advanced button")
    button:SizeToContents()
end)

-- Set active tab
combolist:SetActive("General")

-- Customize appearance
combolist:SetFont("DermaLarge")
combolist:SetTextColor(Color(255, 255, 255))
combolist:SetTextHoverColor(Color(200, 200, 200))
combolist:SetActiveTextColor(Color(255, 255, 0))
combolist:SetAccentColor(Color(0, 150, 255))
combolist:EnableBG(true)
combolist:SetBGColor(Color(50, 50, 50))
```

### Methods

#### Tab Management

| Name                            | Description                                                       |
| ------------------------------- | ----------------------------------------------------------------- |
| AddTab(name, func, customCheck) | Add a new tab with content function and optional visibility check |
| RemoveTab(name)                 | Remove a tab by name                                              |
| SetActive(name, skip\_anim)     | Switch to specified tab with optional animation skip              |
| GetActive()                     | Get the currently active tab name                                 |

#### Content Access

| Name              | Description                            |
| ----------------- | -------------------------------------- |
| GetCurrentPanel() | Get the currently active content panel |
| GetContent()      | Get the main content panel             |
| GetNavBar()       | Get the navigation bar panel           |

#### Appearance

| Name                    | Description                                           |
| ----------------------- | ----------------------------------------------------- |
| SetFont(font)           | Set the font for tab labels                           |
| SetTextColor(col)       | Set the default text color for tabs                   |
| SetTextHoverColor(col)  | Set the text color when hovering over tabs            |
| SetActiveTextColor(col) | Set the text color for the active tab                 |
| SetAccentColor(col)     | Set the accent color for the active tab indicator     |
| EnableBG(bool)          | Enable/disable background painting for navigation bar |
| SetBGColor(col)         | Set the background color for navigation bar           |

#### Callbacks

| Name                   | Description                                   |
| ---------------------- | --------------------------------------------- |
| OnChange(active\_name) | Called when active tab changes (for override) |

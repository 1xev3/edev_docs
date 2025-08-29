---
description: >-
  A VGUI panel that manages multiple pages/panels with switching functionality.
  It can either remove or hide inactive panels based on the configured switch
  method.
---

# esclib.switchmenu

### Usage example

```lua
local switchMenu = vgui.Create("esclib.switchmenu")
switchMenu:SetSwitchMethod("hide") -- or "remove"

-- Add pages with generator functions
switchMenu:AddPage("main", function(panel, w, h)
    local button = panel:Add("DButton")
    button:SetText("Main Page")
    button:SetSize(100, 30)
end)

switchMenu:AddPage("settings", function(panel, w, h)
    local label = panel:Add("DLabel")
    label:SetText("Settings Page")
    label:SetSize(100, 30)
end)

-- Switch between pages
switchMenu:Switch("main")
switchMenu:Switch("settings")

-- Get current active page
local activePage = switchMenu:GetActivePage()
```

### Methods

#### Page Management

| Name                | Description                                      |
| ------------------- | ------------------------------------------------ |
| AddPage(name, func) | Add a new page with generator function           |
| HasPage(name)       | Check if page exists                             |
| GetActivePage()     | Get current active page name                     |
| Switch(name, ...)   | Switch to specified page with optional arguments |

#### Panel Control

| Name         | Description                                        |
| ------------ | -------------------------------------------------- |
| CheckValid() | Remove invalid panels from generated\_panels table |
| Clear()      | Clear all panels (inherited from base panel)       |
| Init()       | Initialize the panel                               |
| Paint()      | Paint function for override                        |

#### Getters

| Name              | Description                                    |
| ----------------- | ---------------------------------------------- |
| GetCurrentPanel() | Get current panel name                         |
| GetSwitchMethod() | Get current switch method ("remove" or "hide") |

#### Setters

| Name                    | Description                            |
| ----------------------- | -------------------------------------- |
| SetCurrentPanel(name)   | Set current panel name                 |
| SetSwitchMethod(method) | Set switch method ("remove" or "hide") |

### Switch Methods

* **"remove"**: Completely removes inactive panels when switching
* **"hide"**: Hides inactive panels and shows only the active one

---
description: >-
  A custom context menu panel for Garry's Mod that provides a modern, scrollable
  interface with support for headers, buttons, separators, and submenus.
---

# esclib.contextmenu

### Usage example

```lua
-- Create context menu
local context = vgui.Create("esclib.contextmenu")

-- Set position near mouse cursor
local x, y = gui.MousePos()
context:SetPosClamped(x, y)

-- Add header
context:AddHeader("Player Actions", Color(255, 255, 255))

-- Add buttons with icons
context:AddButton("Teleport to Player", function(ply)
    print("Teleporting to player: " .. ply:Nick())
end, Material("icon16/user.png"))

-- Add separator
context:AddSeparator()

-- Add submenu
local subButton, subMenu = context:AddSubMenu("Admin Actions", Material("icon16/shield.png"))
subMenu:AddButton("Kick Player", function(ply)
    print("Kicking player: " .. ply:Nick())
end, Material("icon16/door_out.png"))

-- Set max height for scrolling
context:SetMaxHeight(300)

-- Custom close callback
function context:OnClose()
    print("Context menu closed")
end
```

### Methods

#### Getter Methods

| Name                 | Description                                       |
| -------------------- | ------------------------------------------------- |
| GetColor()           | Get the background color of the context menu      |
| GetBorderColor()     | Get the border color of the context menu          |
| GetEnableLayouting() | Get whether automatic layouting is enabled        |
| GetHeaderFont()      | Get the font used for headers                     |
| GetButtonFont()      | Get the font used for buttons                     |
| GetMaxHeight()       | Get the maximum height limit for the context menu |
| GetBorder()          | Get the border size of the context menu           |
| GetPly()             | Get the player associated with this context menu  |

#### Setter Methods

| Name                     | Description                                      |
| ------------------------ | ------------------------------------------------ |
| SetColor(color)          | Set the background color of the context menu     |
| SetBorderColor(color)    | Set the border color of the context menu         |
| SetEnableLayouting(bool) | Enable or disable automatic layouting            |
| SetHeaderFont(font)      | Set the font used for headers                    |
| SetButtonFont(font)      | Set the font used for buttons                    |
| SetMaxHeight(height)     | Set the maximum height limit (0 = no limit)      |
| SetWide(width)           | Set the width of the context menu                |
| SetBorder(border)        | Set the border size of the context menu          |
| SetPly(ply)              | Set the player associated with this context menu |
| SetPosClamped(x, y)      | Set position with screen bounds clamping         |
| SetFont(font)            | Set both header and button fonts                 |

#### Action Methods

| Name                  | Description                                      |
| --------------------- | ------------------------------------------------ |
| Close(anim)           | Close the context menu with optional animation   |
| IsMouseInside()       | Check if mouse cursor is inside the context menu |
| OnClick()             | Override method for click events                 |
| OnClose()             | Override method for close events                 |
| E\_InvalidateLayout() | Recalculate and update the layout                |

#### Content Methods

| Name                        | Description                               |
| --------------------------- | ----------------------------------------- |
| AddButton(text, func, icon) | Add a clickable button with optional icon |
| AddHeader(text, color)      | Add a header text element                 |
| AddSeparator()              | Add a visual separator line               |
| AddSubMenu(text, icon)      | Add a button that opens a submenu         |

### Button Methods (Returned by AddButton)

#### Getter Methods

| Name                | Description                    |
| ------------------- | ------------------------------ |
| GetText()           | Get the button text            |
| GetTextColor()      | Get the normal text color      |
| GetTextHoverColor() | Get the hover text color       |
| GetIconColor()      | Get the normal icon color      |
| GetIconHoverColor() | Get the hover icon color       |
| GetColorHover()     | Get the hover background color |
| GetIcon()           | Get the button icon material   |
| GetFont()           | Get the button font            |
| GetFunc()           | Get the button click function  |

#### Setter Methods

| Name                     | Description                    |
| ------------------------ | ------------------------------ |
| SetText(text)            | Set the button text            |
| SetTextColor(color)      | Set the normal text color      |
| SetTextHoverColor(color) | Set the hover text color       |
| SetIconColor(color)      | Set the normal icon color      |
| SetIconHoverColor(color) | Set the hover icon color       |
| SetColorHover(color)     | Set the hover background color |
| SetIcon(icon)            | Set the button icon material   |
| SetFont(font)            | Set the button font            |
| SetFunc(func)            | Set the button click function  |

### Header Methods (Returned by AddHeader)

#### Getter Methods

| Name           | Description               |
| -------------- | ------------------------- |
| GetTextColor() | Get the header text color |
| GetFont()      | Get the header font       |

#### Setter Methods

| Name                | Description               |
| ------------------- | ------------------------- |
| SetTextColor(color) | Set the header text color |
| SetFont(font)       | Set the header font       |

### Separator Methods (Returned by AddSeparator)

#### Getter Methods

| Name       | Description                  |
| ---------- | ---------------------------- |
| GetColor() | Get the separator line color |

#### Setter Methods

| Name            | Description                  |
| --------------- | ---------------------------- |
| SetColor(color) | Set the separator line color |

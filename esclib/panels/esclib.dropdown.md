---
description: >-
  A customizable dropdown panel for ESCLib that provides a modern dropdown
  interface with hover effects and context menu integration.
---

# esclib.dropdown

### Usage example

```lua
local dropdown = vgui.Create("esclib.dropdown")
dropdown:SetValues({"Option 1", "Option 2", "Option 3"})
dropdown:SetValue("Option 1")
dropdown:SetWide(150)
dropdown:SetTall(30)

function dropdown:OnValueChanged(value)
    print("Selected:", value)
end
```

### Methods

#### Getter Methods

| Name                      | Description                                    |
| ------------------------- | ---------------------------------------------- |
| GetValue()                | Returns the currently selected value           |
| GetValues()               | Returns the table of available options         |
| GetOpened()               | Returns whether the dropdown is currently open |
| GetFont()                 | Returns the font used for text rendering       |
| GetIconFont()             | Returns the font used for the dropdown arrow   |
| GetTextColor()            | Returns the normal text color                  |
| GetTextColorHover()       | Returns the text color when hovered            |
| GetBackgroundColor()      | Returns the normal background color            |
| GetBackgroundColorHover() | Returns the background color when hovered      |
| GetContextParent()        | Returns the parent panel for the context menu  |

#### Setter Methods

| Name                           | Description                                         |
| ------------------------------ | --------------------------------------------------- |
| SetValue(value)                | Sets the selected value and triggers OnValueChanged |
| SetValues(values)              | Sets the available options table                    |
| SetOpened(opened)              | Sets the opened state of the dropdown               |
| SetFont(font)                  | Sets the font for text rendering                    |
| SetIconFont(font)              | Sets the font for the dropdown arrow                |
| SetTextColor(color)            | Sets the normal text color                          |
| SetTextColorHover(color)       | Sets the text color when hovered                    |
| SetBackgroundColor(color)      | Sets the normal background color                    |
| SetBackgroundColorHover(color) | Sets the background color when hovered              |
| SetContextParent(parent)       | Sets the parent panel for the context menu          |

#### Override Methods

| Name                  | Description                                                          |
| --------------------- | -------------------------------------------------------------------- |
| OnClick(context)      | Called when the dropdown is clicked, receives the context menu panel |
| OnValueChanged(value) | Called when the selected value changes                               |

#### Utility Methods

| Name             | Description                                       |
| ---------------- | ------------------------------------------------- |
| DoClick()        | Opens the dropdown context menu                   |
| IsOpened()       | Returns whether the dropdown is currently open    |
| SizeToContents() | Automatically sizes the dropdown based on content |

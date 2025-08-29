---
description: >-
  A custom VGUI panel that combines a slider with a text entry for numeric
  input. This panel allows users to adjust values using either the slider or by
  typing directly into the text field.
---

# esclib.numslider

### Usage example

```lua
local numslider = vgui.Create("esclib.numslider")
numslider:SetMin(0)
numslider:SetMax(100)
numslider:SetValue(50)
numslider:SetDecimals(2)
numslider:SetStep(5)

numslider.OnValueChanged = function(panel, newValue)
    print("Value changed to: " .. newValue)
end
```

### Methods

#### Getter Methods

| Name       | Description                                     |
| ---------- | ----------------------------------------------- |
| GetValue() | Returns the current numeric value of the slider |
| GetMin()   | Returns the minimum value of the slider         |
| GetMax()   | Returns the maximum value of the slider         |

#### Setter Methods

| Name             | Description                                         |
| ---------------- | --------------------------------------------------- |
| SetValue(num)    | Sets the current value of the slider and text entry |
| SetMin(num)      | Sets the minimum value of the slider                |
| SetMax(num)      | Sets the maximum value of the slider                |
| SetDecimals(num) | Sets the number of decimal places for the slider    |
| SetStep(num)     | Sets the step increment for the slider              |
| SetBG(panel)     | Sets the parent panel for keyboard input handling   |

#### Event Methods

| Name                | Description                                                                   |
| ------------------- | ----------------------------------------------------------------------------- |
| OnValueChanged(new) | Called when the value changes. Override this function to handle value changes |
| OnSizeChanged(w, h) | Called when the panel size changes. Invalidates the parent layout             |

#### Internal Methods

| Name   | Description                                                         |
| ------ | ------------------------------------------------------------------- |
| Init() | Initializes the panel, creates the slider and text entry components |

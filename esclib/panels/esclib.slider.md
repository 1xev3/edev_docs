---
description: >-
  A custom slider panel that extends the default DSlider with enhanced visual
  styling and functionality.
---

# esclib.slider

### Usage example

```lua
local slider = vgui.Create("esclib.slider")
slider:SetSize(200, 30)
slider:SetMin(0)
slider:SetMax(100)
slider:SetValue(50)
slider:SetDecimals(0)
slider:SetScrollStep(5)

slider.OnValueChanged = function(self, value)
    print("Slider value changed to: " .. value)
end
```

### Methods

#### Getter Methods

| Name            | Description                                                     |
| --------------- | --------------------------------------------------------------- |
| GetDecimals()   | Returns the number of decimal places for the slider value       |
| GetScrollStep() | Returns the scroll step value for mouse wheel scrolling         |
| GetMin()        | Returns the minimum value of the slider                         |
| GetMax()        | Returns the maximum value of the slider                         |
| GetValue()      | Returns the current slider value with decimal precision applied |

#### Setter Methods

| Name               | Description                                                            |
| ------------------ | ---------------------------------------------------------------------- |
| SetDecimals(num)   | Sets the number of decimal places for the slider value                 |
| SetScrollStep(num) | Sets the scroll step value for mouse wheel scrolling                   |
| SetMin(num)        | Sets the minimum value of the slider (clamped to not exceed max)       |
| SetMax(num)        | Sets the maximum value of the slider (clamped to not be less than min) |
| SetValue(num)      | Sets the current slider value (clamped between min and max)            |

#### Event Methods

| Name                  | Description                                                              |
| --------------------- | ------------------------------------------------------------------------ |
| OnValueChanged(value) | Called when the slider value changes (override this for custom behavior) |
| OnMouseWheeled(delta) | Handles mouse wheel scrolling to adjust slider value                     |
| OnSizeChanged(w, h)   | Called when the panel size changes, adjusts knob height                  |

#### Override Methods

| Name        | Description                                                                         |
| ----------- | ----------------------------------------------------------------------------------- |
| Paint(w, h) | Custom painting method that draws the slider with rounded corners and hover effects |
| Init()      | Initializes the slider with default values and cursor behavior                      |

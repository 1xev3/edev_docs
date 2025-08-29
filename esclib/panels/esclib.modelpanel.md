---
description: >-
  A custom model panel that extends the default DModelPanel with enhanced
  rendering capabilities and mouse interaction features. This panel provides
  better handling of off-screen rendering and includes
---

# esclib.modelpanel

### Usage example

```lua
local modelPanel = vgui.Create("esclib.modelpanel")
modelPanel:SetSize(200, 200)
modelPanel:SetModel("models/props_junk/wooden_box01a.mdl")
modelPanel:EnableMouseDragging(function(panel)
    -- Custom layout callback
    local ent = panel:GetEntity()
    if IsValid(ent) then
        ent:SetAngles(Angle(0, RealTime() * 50, 0))
    end
end)
```

### Methods

#### Core Methods

| Name              | Description                                                                  |
| ----------------- | ---------------------------------------------------------------------------- |
| Init()            | Initializes the panel (currently empty, for override purposes)               |
| BeforePaint(w, h) | Called before painting, can be overridden for custom pre-paint logic         |
| Paint(w, h)       | Main painting function that handles 3D rendering with off-screen adjustments |
| DrawModel()       | Draws the model with proper scissor rect handling and parent clipping        |
| LayoutEntity(ent) | Layout function for the entity, can be customized via EnableMouseDragging    |

#### Mouse Interaction Methods

| Name                          | Description                                                 |
| ----------------------------- | ----------------------------------------------------------- |
| EnableMouseDragging(callback) | Enables mouse dragging functionality with optional callback |
| OnMousePressed()              | Handles mouse press events for dragging                     |
| OnMouseReleased()             | Handles mouse release events and resets cursor position     |
| OnMouseWheeled(delta)         | Handles mouse wheel events for FOV adjustment               |

#### Mouse Interaction Properties

| Name           | Description                                         |
| -------------- | --------------------------------------------------- |
| mouseinput     | Boolean indicating if mouse dragging is active      |
| mousex, mousey | Current mouse cursor position                       |
| startx, starty | Initial mouse cursor position when dragging started |

#### Rendering Properties

| Name             | Description                           |
| ---------------- | ------------------------------------- |
| LastPaint        | Timestamp of the last paint operation |
| aLookAngle       | Camera look angle                     |
| vLookatPos       | Camera look-at position               |
| vCamPos          | Camera position                       |
| fFOV             | Field of view                         |
| FarZ             | Far clipping plane                    |
| colAmbientLight  | Ambient lighting color                |
| colColor         | Model color modulation                |
| DirectionalLight | Array of directional light colors     |
| Entity           | The model entity being rendered       |

#### Inherited DModelPanel Methods

This panel inherits all methods from DModelPanel, including:

| Name                | Description                       |
| ------------------- | --------------------------------- |
| SetModel(modelPath) | Sets the model to display         |
| SetEntity(entity)   | Sets the entity to render         |
| SetFOV(fov)         | Sets the field of view            |
| GetFOV()            | Gets the current field of view    |
| SetCamPos(position) | Sets the camera position          |
| SetLookAt(position) | Sets the look-at position         |
| SetAngles(angles)   | Sets the camera angles            |
| GetEntity()         | Gets the current entity           |
| GetCamPos()         | Gets the current camera position  |
| GetLookAt()         | Gets the current look-at position |
| GetAngles()         | Gets the current camera angles    |

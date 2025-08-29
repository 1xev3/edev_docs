---
description: >-
  A circular avatar panel that displays Steam avatars with a circular mask using
  stencil rendering.
---

# esclib.circle\_avatar

### Usage example

```lua
local avatar = vgui.Create("esclib.circle_avatar")
avatar:SetSize(64, 64)
avatar:SetSteamID("STEAM_0:1:12345678")
-- or
avatar:SetPlayer(player.GetByID(1))
avatar:SetPolyCount(32) -- Increase polygon count for smoother circle
```

### Methods

#### Getter Methods

| Name           | Description                                                     |
| -------------- | --------------------------------------------------------------- |
| GetPolyCount() | Returns the number of polygons used to create the circular mask |

#### Setter Methods

| Name                | Description                                                                                                                |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| SetPolyCount(count) | Sets the number of polygons used to create the circular mask. Higher values create smoother circles but impact performance |
| SetSteamID(steamid) | Sets the avatar to display using a Steam ID                                                                                |
| SetPlayer(player)   | Sets the avatar to display using a player entity                                                                           |

#### Internal Methods

| Name                    | Description                                                                             |
| ----------------------- | --------------------------------------------------------------------------------------- |
| Init()                  | Initializes the panel, creates the avatar image and sets default poly count             |
| MakePoly(x, y, w, h)    | Creates a circular polygon mask for the given rectangle                                 |
| MakeCirclePoly(x, y, r) | Creates a circular polygon with specified center and radius                             |
| PerformLayout()         | Handles layout changes and triggers size recalculation                                  |
| OnSizeChanged(w, h)     | Called when panel size changes, updates avatar size and regenerates polygon mask        |
| DrawMask(w, h)          | Draws the circular stencil mask                                                         |
| DrawBackground(w, h)    | Virtual method for drawing background (can be overridden)                               |
| Paint(w, h)             | Main paint function that renders the avatar with circular mask using stencil operations |

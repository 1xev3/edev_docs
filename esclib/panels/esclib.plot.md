---
description: >-
  A comprehensive plotting panel for Garry's Mod that supports multiple chart
  types including line plots, histograms, and pie charts. Features include
  tooltips, legends, grid lines, and customizable sty
---

# esclib.plot

### Usage example

```lua
local plot = vgui.Create("esclib.plot")
plot:SetSize(400, 300)
plot:SetDisplayMode("plot") -- or "histogram" or "pie"
plot:SetDrawGrid(true)
plot:SetDrawPoints(true)
plot:SetShowLegend(true)
plot:SetLegendPosition("topright")
plot:SetEnableTooltip(true)

-- For line plots and histograms
local xPoints = {1, 2, 3, 4, 5}
local yPoints = {10, 20, 15, 25, 30}
plot:AddSeries("Data Series", xPoints, yPoints, Color(50, 150, 250))

-- For pie charts
plot:SetDisplayMode("pie")
plot:AddSeries("Segment 1", 155, nil, Color(50, 150, 250))
plot:AddSeries("Segment 2", 25, nil, Color(255, 100, 100))
```

### Methods

#### Data Management

| Name                                     | Description                                                                                |
| ---------------------------------------- | ------------------------------------------------------------------------------------------ |
| AddSeries(name, xPoints, yPoints, color) | Add a new data series to the plot. For pie charts, xPoints should be a single number value |
| ClearSeries()                            | Remove all data series from the plot                                                       |
| GetSeries()                              | Get all series data                                                                        |
| GetSeriesCount()                         | Get the number of series in the plot                                                       |
| SetXPoints(tbl)                          | Set X points for the first series                                                          |
| SetYPoints(tbl)                          | Set Y points for the first series                                                          |

#### Display Configuration

| Name                        | Description                                                             |
| --------------------------- | ----------------------------------------------------------------------- |
| SetDisplayMode(mode)        | Set the chart type: "plot", "histogram", or "pie"                       |
| SetDrawGrid(enabled)        | Enable or disable grid lines                                            |
| SetDrawPoints(enabled)      | Enable or disable point markers on line plots                           |
| SetShowLegend(enabled)      | Show or hide the legend                                                 |
| SetLegendPosition(position) | Set legend position: "topleft", "topright", "bottomleft", "bottomright" |
| SetEnableTooltip(enabled)   | Enable or disable tooltips on hover                                     |
| SetInnerRadius(radius)      | Set inner radius for pie charts (0.0 to 1.0)                            |

#### Formatting

| Name                   | Description                           |
| ---------------------- | ------------------------------------- |
| SetXFormat(format)     | Set format string for X axis labels   |
| SetYFormat(format)     | Set format string for Y axis labels   |
| SetMargin(margin)      | Set margin around the plot area       |
| SetBarPadding(padding) | Set padding between bars in histogram |
| SetXTicks(count)       | Set number of X axis tick marks       |
| SetYTicks(count)       | Set number of Y axis tick marks       |

#### Interpolation

| Name                                                  | Description                                                      |
| ----------------------------------------------------- | ---------------------------------------------------------------- |
| InterpolatePoints(method, density)                    | Interpolate all series points using specified method and density |
| InterpolateSeriesPoints(seriesIndex, method, density) | Interpolate specific series points                               |

#### Getters

| Name                | Description                 |
| ------------------- | --------------------------- |
| GetDisplayMode()    | Get current display mode    |
| GetDrawGrid()       | Get grid drawing state      |
| GetDrawPoints()     | Get point drawing state     |
| GetShowLegend()     | Get legend visibility state |
| GetLegendPosition() | Get legend position         |
| GetEnableTooltip()  | Get tooltip state           |
| GetInnerRadius()    | Get pie chart inner radius  |
| GetXFormat()        | Get X axis format string    |
| GetYFormat()        | Get Y axis format string    |
| GetMargin()         | Get plot margin             |
| GetBarPadding()     | Get bar padding             |
| GetXTicks()         | Get X axis tick count       |
| GetYTicks()         | Get Y axis tick count       |

#### Setters

| Name                        | Description                |
| --------------------------- | -------------------------- |
| SetDisplayMode(mode)        | Set display mode           |
| SetDrawGrid(enabled)        | Set grid drawing state     |
| SetDrawPoints(enabled)      | Set point drawing state    |
| SetShowLegend(enabled)      | Set legend visibility      |
| SetLegendPosition(position) | Set legend position        |
| SetEnableTooltip(enabled)   | Set tooltip state          |
| SetInnerRadius(radius)      | Set pie chart inner radius |
| SetXFormat(format)          | Set X axis format string   |
| SetYFormat(format)          | Set Y axis format string   |
| SetMargin(margin)           | Set plot margin            |
| SetBarPadding(padding)      | Set bar padding            |
| SetXTicks(count)            | Set X axis tick count      |
| SetYTicks(count)            | Set Y axis tick count      |

### Chart Types

#### Line Plot

* Displays data as connected line segments
* Supports multiple series with different colors
* Optional point markers at data points
* Grid lines and axis labels

#### Histogram

* Displays data as vertical bars
* Supports multiple series with grouped bars
* Automatic bar spacing and sizing
* Grid lines and axis labels

#### Pie Chart

* Displays data as circular segments
* Each series represents a segment with percentage
* Optional inner radius for donut effect
* Text labels on segments (if large enough)
* Legend shows percentages

### Features

* **Tooltips**: Hover over data points to see exact values
* **Legend**: Configurable legend with position options
* **Grid**: Optional grid lines for better readability
* **Formatting**: Customizable number formats for axis labels
* **Interpolation**: Smooth line interpolation between points
* **Responsive**: Adapts to panel size changes
* **Performance**: Cached calculations for smooth rendering

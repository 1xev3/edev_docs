---
description: Client side
icon: wrench
---

# esclib.utils

```lua
function esclib.util:TruncateStr(str: string, maxLength: number) -> string
```

Trims the string to a specified length, appending "..." if the string exceeds the length.

***

```lua
function esclib.util:IsRestrictedChar(strs: string) -> boolean
```

Checks for restricted characters in a string and returns true if found.

***

```lua
function esclib.util:HexToColor(hex: string, alpha: number) -> Color
```

Converts a hex color string to a Color object with specified transparency.

***

```lua
function esclib.util.PrecacheArc(cx: number, cy: number, radius: number, thickness: number, startang: number, endang: number, roughness: number, rote: number) -> table
```

Returns a table of points representing an arc with specified parameters.

***

```lua
function esclib.util:NumberLimit(number: number, min: number, max: number, str_format: string) -> string
```

Limits a number between given bounds and formats it as a string.

***

```lua
function esclib.util:NiceTime(time: number, bHours: boolean, bMinutes: boolean, bSeconds: boolean, bMilliseconds: boolean, try_language: string) -> string
```

Formats the given time considering selected display of hours, minutes, seconds, and milliseconds.

***

```lua
function esclib.util:Round(x: number) -> number
```

Rounds a number to the nearest integer.

***

```lua
function esclib.util:TextCutAccurate(text: string, font: string, maxw: number, add_symbol: string)
```

Accurately trims text to a specified pixel width, adding a symbol if text was trimmed.

***

```lua
function esclib.util:TextCut(text: string, font: string, maxw: number, add_symbol: string)
```

Similarly trims text by width, but might differ in processing accuracy.

***

```lua
function esclib.util:TextSize(txt: string, font: string) -> number, number
```

Returns the width and height of the text in pixels for the specified font.

***

```lua
function esclib.util:IsValuesEqual(var1: any, var2: any) -> boolean
```

Compares two values and returns true if they are equal, otherwise false.

***

```lua
function esclib.util:ColorMean(...) -> Color
```

Calculates the mean color value from input colors and returns the resulting color.

***

```lua
function esclib.util:PrecacheRoundedPoly(x: number, y: number, w: number, h: number, radius: number, cornerPoints: number) -> table
```

Returns a table containing the coordinates of points for drawing a rounded polygon.


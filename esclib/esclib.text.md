---
icon: text-size
---

# esclib.text

```lua
function esclib.text:Multiline(text: string, font: string, mWidth: number, interval: number) -> table ome code
```

Splits a long text string into multiple lines based on the maximum width and specified interval, returning line data with formatting information.

***

```lua
function esclib.text:MultilineToString(multiline_data: table) -> string 
```

Concatenates the lines of multiline data into a single string with newline separators.

***

```lua
function esclib.text:DrawMultiline(multiline_data: table, x: number, y: number, color: table, alignX: number, alignY: number) 
```

Draws multiple lines of text at the specified position with alignment and color.

***

```lua
function esclib.text:DrawMultilineShadow(multiline_data: table, x: number, y: number, color: table, alignX: number, alignY: number, offsetx: number) 
```

Draws multiline text with a shadow effect by offsetting the text slightly.

***

```lua
function esclib.text:Capitalize(str: string) -> string 
```

Capitalizes the first letter of a string.

***

```lua
function esclib.text:KeyFormat(formatString: string, replacements: table) -> string 
```

Replaces placeholders in a format string with values from a table.

***

```lua
function esclib.text:MatchSplit(str: string, pattern: string) -> table 
```

Splits a string into matched and unmatched segments based on a specified pattern, returning a structured table of results.

***

```lua
function esclib.text.distance(str1: string, str2: string) -> number 
```

Calculates the Levenshtein distance between two strings, representing the minimum number of edits needed to transform one string into the other.


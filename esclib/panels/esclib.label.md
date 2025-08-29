---
description: >-
  A custom VGUI label panel that supports colored text, text parsing with color
  tags, automatic text wrapping, and shadow effects.
---

# esclib.label

### Usage example

```lua
local label = vgui.Create("esclib.label")
label:SetDrawShadow(true)
label:SetFont(esclib:AdaptiveFont("esclib", 20, 500))
label:SetMaxDimensions(500, 1000)
label:SetText(Color(255,0,0), "Hello", Color(0,255,0), "World")
label:SetTextParsed("Привет, <frame.bg>Мир! <green>sit amet <yellow>consectetur</>")
```

### Methods

#### Text and Content Methods

| Name                | Description                                                       |
| ------------------- | ----------------------------------------------------------------- |
| SetText(...)        | Set text content with optional colors. Accepts multiple arguments |
| AppendText(text)    | Add text to the end of current content                            |
| AppendColor(color)  | Add a color to the end of current content                         |
| SetTextParsed(text) | Parse text with color tags like `<red>`, `<green>`, `<frame.bg>`  |
| GetText()           | Get the raw text array                                            |

#### Font and Styling Methods

| Name                   | Description                     |
| ---------------------- | ------------------------------- |
| SetFont(font)          | Set the font for text rendering |
| GetFont()              | Get the current font            |
| SetTextColor(color)    | Set the default text color      |
| GetTextColor()         | Get the default text color      |
| SetDrawShadow(boolean) | Enable/disable text shadow      |
| GetDrawShadow()        | Get shadow drawing state        |
| SetColors(colors)      | Set addon colors for parsing    |
| GetColors()            | Get addon colors                |

#### Dimension and Layout Methods

| Name                                  | Description                                    |
| ------------------------------------- | ---------------------------------------------- |
| SetMaxDimensions(maxWidth, maxHeight) | Set maximum width and height for text wrapping |
| SetMaxWidth(maxWidth)                 | Set maximum width for text wrapping            |
| SetMaxHeight(maxHeight)               | Set maximum height for text wrapping           |
| SetLineOffset(offset)                 | Set additional spacing between lines           |
| GetLineOffset()                       | Get the current line offset                    |
| GetTextSize()                         | Get the calculated text width and height       |
| GetTextWidth()                        | Get the calculated text width                  |
| GetTextHeight()                       | Get the calculated text height                 |

#### Text Parsing Features

The panel supports color parsing with the following syntax:

* <mark style="color:red;">`<red>`</mark>, <mark style="color:green;">`<green>`</mark>, <mark style="color:blue;">`<blue>`</mark>, <mark style="color:yellow;">`<yellow>`</mark>, <mark style="color:orange;">`<orange>`</mark>, <mark style="color:purple;">`<purple>`</mark>, <mark style="color:$primary;">`<pink>`</mark>, `<cyan>`, `<white>`, `<black>`, `<gold>`, `<silver>`, `<gray>` - Built-in colors
* `<frame.bg>`, `<button.text>` - Addon colors (nested dot notation)
* `</>` or `<\>` - Reset to default text color
* `\n` - New line character

#### Automatic Features

* **Text Wrapping**: Automatically wraps text to fit within max dimensions
* **Ellipsis**: Adds "..." when text exceeds max height
* **Word Breaking**: Breaks words at spaces when wrapping
* **Multi-line Support**: Handles multiple lines with proper spacing
* **Color Segments**: Maintains color information for each text segment

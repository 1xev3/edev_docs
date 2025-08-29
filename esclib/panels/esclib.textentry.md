---
description: >-
  A custom text entry panel that extends EditablePanel with enhanced styling and
  functionality.
---

# esclib.textentry

### Usage example

```lua
local textentry = vgui.Create("esclib.textentry")
textentry:SetPlaceholderText("Enter text here...")
textentry:SetText("Initial text")
textentry:SetFont("DermaLarge")
textentry:SetBorder(5)
textentry:SetInputPanel(some_panel)
```

### Methods

#### Getter Methods

| Name                   | Description                                                |
| ---------------------- | ---------------------------------------------------------- |
| GetPlaceholderText()   | Get the placeholder text displayed when the entry is empty |
| GetBackgroundColor()   | Get the main background color                              |
| GetBackgroundColor2()  | Get the secondary background color (used for outer border) |
| GetTextColor()         | Get the text color                                         |
| GetTextColorGray()     | Get the placeholder text color                             |
| GetTextColorSelected() | Get the selected text color                                |
| GetFont()              | Get the current font                                       |
| GetText()              | Get the current text value                                 |
| GetBorder()            | Get the current border size                                |
| GetTextEntry()         | Get the underlying DTextEntry panel                        |

#### Setter Methods

| Name                        | Description                                                |
| --------------------------- | ---------------------------------------------------------- |
| SetPlaceholderText(text)    | Set the placeholder text displayed when the entry is empty |
| SetBackgroundColor(color)   | Set the main background color                              |
| SetBackgroundColor2(color)  | Set the secondary background color (used for outer border) |
| SetTextColor(color)         | Set the text color                                         |
| SetTextColorGray(color)     | Set the placeholder text color                             |
| SetTextColorSelected(color) | Set the selected text color                                |
| SetFont(font)               | Set the font for the text entry                            |
| SetText(text)               | Set the text value                                         |
| SetBorder(val)              | Set the border size around the text entry                  |
| SetInputPanel(pnl)          | Set the panel that will receive keyboard input focus       |

#### Other Methods

| Name                      | Description                                        |
| ------------------------- | -------------------------------------------------- |
| Init()                    | Initialize the panel (called automatically)        |
| OnMousePressed(mousecode) | Handle mouse press events and focus the text entry |
| Paint(w, h)               | Render the panel with rounded background           |

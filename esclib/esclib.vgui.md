---
description: Client side
icon: table-columns
---

# esclib.vgui

```lua
function PANEL_META:eSetHoverPanel(generate_panel: bool)
```

```lua
function PANEL_META:eAddHint(text: string, font: string, align: TEXT_ALIGN, parent_panel: panel)
```

```lua
function esclib:GenerateBGClicker(key_input: bool)
```

```lua
function esclib:GeneratePopWindow(key_input: bool)
```

```lua
function esclib:TextInputWindow(title, text, is_multiline, is_numeric, callback, custom_check, try_language)
```

```lua
function esclib:ConfirmWindow(title, text, callback)
```

```lua
function esclib:ChoiceMenu(title,items,max_selections,item_paint,callback,custom_filter,need_search,selected_values, wide)
```

```lua
function esclib:PlayerSelectWindow(title,multi,hide_self,callback,custom_filter)
```

```lua
function esclib:NewAnimation(length, delay, ease, onend, think_fn)
```

# TranslateIf

## Usage example
```lua
local result = addon:TranslateIf("#welcome") -- Translates
local result = addon:TranslateIf("Hello") -- Returns as-is
```

## Args:
1. **string** var - The text to potentially translate

## Return values:
1. **string** - Translated text if key starts with "#", otherwise original text

## Notes
Conditionally translates text only if it starts with "#" (indicating a translation key).

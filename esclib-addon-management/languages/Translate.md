# Translate

## Usage example
```lua
local translated = addon:Translate("welcome", "ru")
local translated = addon:Translate("welcome") -- Uses current language
```

## Args:
1. **string** var - The translation key to look up
2. **string** lang - The language code (optional, defaults to current language)

## Return values:
1. **string** - The translated text or "#key" if not found

## Notes
Translates a key to the specified language. Falls back to default language if key not found in requested language.

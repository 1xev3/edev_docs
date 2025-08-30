# CanTranslate

## Usage example
```lua
if addon:CanTranslate("welcome", "ru") then
    -- Russian translation exists
end
```

## Args:
1. **string** var - The translation key to check
2. **string** lang - The language code (optional, defaults to current language)

## Return values:
1. **boolean** - True if translation exists, false otherwise

## Notes
Checks if a translation key exists in the specified language.

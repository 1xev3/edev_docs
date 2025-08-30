# RegisterLanguages

## Usage example
```lua
addon:RegisterLanguages({
    ["en"] = {
        ["welcome"] = "Welcome!",
        ["goodbye"] = "Goodbye!"
    },
    ["ru"] = {
        ["welcome"] = "Добро пожаловать!",
        ["goodbye"] = "До свидания!"
    }
})
```

## Args:
1. **table** langs - The languages table to register

## Notes
Registers language strings for the addon. Merges with existing languages.

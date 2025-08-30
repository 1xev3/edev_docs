# DownloadMaterial

## Usage example
```lua
addon:DownloadMaterial("http://example.com/image.png", 
    function(success) print("Downloaded!") end,
    function(error) print("Failed:", error) end,
    3, "textures")
```

## Args:
1. **string** url - The URL to download the material from
2. **function** on_succ - Success callback function
3. **function** on_err - Error callback function
4. **number** retry_count - Number of retry attempts
5. **string** additional_path - Additional subfolder path

## Notes
Downloads a material from URL and saves it locally. Only available on client-side.

# NetReadCompressedTable

## Usage example
```lua
local data = esclib:NetReadCompressedTable(16, true)
```

## Args:
1. **number** bits - Number of bits for size (default: 16)
2. **boolean** pretty - Whether to use pretty JSON parsing

## Return values:
1. **table** - The decompressed and parsed table

## Notes
Reads and decompresses a table from the network stream. Must be called in the same order as NetWriteCompressedTable.

# NetWriteCompressedTable

## Usage example
```lua
esclib:NetWriteCompressedTable(data_table, 16)
```

## Args:
1. **table** to_send - The table to compress and send
2. **number** bits - Number of bits for size (default: 16)

## Notes
Compresses a table using JSON compression and writes it to the network stream. Useful for sending large data efficiently over the network.

# SafeMerge

## Usage example
```lua
esclib:SafeMerge(table1, table2, forceOverride)
```

## Args:
1. **table** table1 - The target table to merge into
2. **table** table2 - The source table to merge from
3. **boolean** forceOverride - Whether to force override existing values

## Return values:
1. **table** - The merged table (same reference as table1)

## Notes
This function safely merges two tables while detecting cycles to prevent infinite recursion. It recursively merges nested tables and handles the merge operation safely.

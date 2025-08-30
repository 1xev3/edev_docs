# SyncVars

## Usage example
```lua
addon:SyncVars(1)  -- Settings -> vars
addon:SyncVars(-1) -- Vars -> settings
```

## Args:
1. **number** direction - Direction of synchronization (>= 0: settings->vars, < 0: vars->settings)

## Notes
Synchronizes variables between the vars table and the wrapped settings structure.

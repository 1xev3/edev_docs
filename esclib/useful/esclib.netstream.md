---
icon: signal-stream
---

# esclib.netstream

### Send from <mark style="color:blue;">server</mark> side

```lua
--Start on server
netstream.Start(recievers: table, name: string, vararg ...)
--Recieve on client
netstream.Hook(name, on_recieved: function(vararg ...))
```

### Send from <mark style="color:orange;">client</mark> side

```lua
--Start on client
netstream.Start(name: string, vararg ...)
--Recieve on server
netstream.Hook(name, on_recieved: function(vararg ...))
```

### Example <mark style="color:blue;">server</mark> side

```lua
local netstream = esclib.netstream
if SERVER then
    local PLAYER_META = FindMetaTable("Player")
    function PLAYER_META:EsclibChatPrint(...)
        netstream.Start(self, "esclib.message", ...)
    end
else --CLIENT
    netstream.Hook("esclib.message", function(...)
	chat.AddText(...)
    end)
end
```


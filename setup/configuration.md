# ⚙ Configuration

{% code title="Configuration" %}
```lua
return {
    Stocking = {
        Enabled = true, -- Is the actual stocking system enabled? Change to false to disable.

        Group = 14196949, -- Group Identifier (https://roblox.com/groups/ID/name)
        Whitelisted = {200, 250, 254, 255}, -- Valid rolesets able to gain the restock tool.

        RestrictAmount = true, -- Restrict the amount of a certain product to one.
        MaxDistance = 15 -- How far away can someone be from an item to restock it. (studs)
    },

    Types = {
        ClickDetector = false, -- Use ClickDetectors to pick up items
        ProximityPrompt = true -- Use ProximityPrompts to pick up items
    }
}
```
{% endcode %}

# Plugins

stockLogic automatically ships two plugins, an example plugin, and a plugin called interface - which shows a `BillboardGui` when an item is out of stock.

You can create a plugin by creating a `ModuleScript` and parenting it to the `Plugins` folder in `Deploy`. Your plugin is expected to return a functions, with the parameters `Events` and `Configuration`. Our events are listed below.

{% tabs %}
{% tab title="Restock" %}
`Player: Player`, `Category: Folder`, `Product: Instance`

```lua
Events.Restock:Connect(function(Player, Category, Product)
    print(Player.Name, ' restocked ', Category.Name)
end)
```
{% endtab %}

{% tab title="Pickup" %}
`Player: Player`, `Category: Folder`, `Product: Instance`

```lua
Events.Pickup:Connect(function(Player, Category, Product)
    print(Player.Name, ' picked up ', Category.Name)
end)
```
{% endtab %}

{% tab title="SupplyToolPickup" %}
```lua
Events.SupplyToolPickup:Connect(function(Player)
    print(Player.Name, ' picked up the supply tool.')
end)
```
{% endtab %}
{% endtabs %}

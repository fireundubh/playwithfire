<!-- TITLE: Passing the player reference to the Activate function -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Passing the player reference to the Activate function
## Anti-pattern

The author of the code below passes the player reference to the `Activate` function to loot an item to the player's inventory.

```
If kItem != None
	kItem.Activate(Game.GetPlayer())
EndIf
```

There is a game engine issue where if the player reference is passed as the activator to the `Activate` function, the game may crash or freeze for some players, especially if this function is executed rapidly and frequently.

## Best practice

1. Create an off-stage dummy cell with a dummy NPC.
2. Pass the dummy NPC as the activator to the `Activate` function.
3. Attach a script to the dummy NPC that transfer items from the dummy NPC to the player.

```
Actor Property PlayerRef Auto

Event OnInit()
	AddInventoryEventFilter(None)
EndEvent

Event OnItemAdded(Form akBaseItem, Int aiItemCount, ObjectReference akItemReference, ObjectReference akSourceContainer)
	Self.RemoveItem(akBaseItem, aiItemCount, False, PlayerRef)
EndEvent
```
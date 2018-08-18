<!-- TITLE: Using a variable to store a property value used once -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Using a variable to store a property value used once
## Anti-pattern

The author of the code below declares a reusable variable to store a property value but the variable is used in only one code path.

```
GlobalVariable Property SendMessage Auto Const

Function DoSomething(Int aiItemCount)
	Bool ShouldNotify = SendMessage.Value as Bool
	
	If aiItemCount > 5
		SendMessageToPlayer(asMessage, ShouldNotify)
	Else
		SendMessageToPlayer(asMessage, False)
	EndIf
EndEvent
```

## Best practice

If a property value is used in only one code path, reference the property value directly. The code above can be simplified like so:

```
GlobalVariable Property SendMessage Auto Const

Function DoSomething(Int aiItemCount)	
	If aiItemCount > 5
		SendMessageToPlayer(asMessage, SendMessage.Value as Bool)
	Else
		SendMessageToPlayer(asMessage, False)
	EndIf
EndEvent
```
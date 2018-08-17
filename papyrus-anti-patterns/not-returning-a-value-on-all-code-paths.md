<!-- TITLE: Not returning a value on all code paths -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Not returning a value on all code paths

## Anti-pattern

The author of the code below returns a value on two code paths, but the functon has three code paths.

```
Bool Function ItemCanBeProcessed(ObjectReference akItem)
	If akItem.Is3DLoaded() && !akItem.IsDisabled() && !akItem.IsDeleted() && !akItem.IsDestroyed() && !akItem.IsActivationBlocked()
		Return True
	Else
		Return False
	EndIf
EndFunction
```

Papyrus raises a warning without an accompanying error:

```
warning: Assigning None to an non-object variable named "::temp21"
```

## Best practice

Ensure that all code paths return a value. The above code could be written like so:

```
Bool Function ItemCanBeProcessed(ObjectReference akItem)
	If akItem.Is3DLoaded() && !akItem.IsDisabled() && !akItem.IsDeleted() && !akItem.IsDestroyed() && !akItem.IsActivationBlocked()
		Return True
	EndIf
	
	Return False
EndFunction
```
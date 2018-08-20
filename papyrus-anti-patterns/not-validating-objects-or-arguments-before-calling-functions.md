<!-- TITLE: Not validating objects or arguments before calling functions -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Not validating objects or arguments before calling functions
## Anti-pattern

The author of the code below calls a function without checking whether the arguments are correct.

```
Int i = 0

While (i < ItemArray.Length)
	ObjectReference kItem = ItemArray.GetAt(i) as ObjectReference
	
	kItem.Activate(DummyRef)
	
	i += 1
EndWhile
```

## Best practice

If an object or argument could become `None` or any other undesirable value, check the variable before the function call.

```
Int i = 0

While (i < ItemArray.Length)
	ObjectReference kItem = ItemArray.GetAt(i) as ObjectReference
	
	If (kItem != None) && (DummyRef != None)
		kItem.Activate(DummyRef)
	EndIf
	
	i += 1
EndWhile
```

Otherwise, Papyrus will abort the function call and you will see this error in the log:

> Cannot call Activate() on a None object, aborting function call
<!-- TITLE: Not validating objects or arguments before calling functions -->

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

If an object or argument becomes `None` prior to the function call, Papyrus will abort the function call and log the following error:

> error: Cannot call `Activate()` on a `None` object, aborting function call

## Best practice

Check the variable or variables for `None` before the function call.

```
Int i = 0

While (i < ItemArray.Length)
	ObjectReference kItem = ItemArray[i] as ObjectReference

	If (kItem != None) && (DummyRef != None)
		kItem.Activate(DummyRef)
	EndIf

	i += 1
EndWhile
```
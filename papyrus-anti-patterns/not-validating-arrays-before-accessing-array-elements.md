<!-- TITLE: Not validating arrays before accessing array elements -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Not validating arrays before accessing array elements
## Anti-pattern

The author of the code below attempts to access an element of an array without checking whether the array exists.

```
Int i = 0

While (i < ItemArray.Length)
	ObjectReference kItem = ItemArray[i] as ObjectReference
	
	; do stuff
	
	i += 1
EndWhile
```

## Best practice

If you try to access an element of a `None` array, Papyrus will log the following error:

> Cannot access an element of a `None` array

Check that the array exists before accessing elements of that array.

```
If ItemArray != None
	Int i = 0
	
	While (ItemArray.Length > 0) && (i < ItemArray.Length)
		ObjectReference kItem = ItemArray[i] as ObjectReference

		; do stuff

		i += 1
	EndWhile
EndIf
```

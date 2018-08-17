<!-- TITLE: Not validating the length of a dynamic array -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Not validating the length of a dynamic array
## Anti-pattern

A dynamic array is a new feature introduced by Fallout 4. Dynamic arrays can be created by passing zero to the array length. For example:

```
ObjectReference[] kResult = new ObjectReference[0]
```

Unlike arrays returned by native functions and editor-filled array properties, dynamic arrays are limited to 128 items.

The author of the code below uses a loop to iterate through a native array and add items to a dynamic array without validing the length of the dynamic array.

> **Editorial Note:** For the sake of clarity, some best practices are ignored in this example.

```
ObjectReference[] kResult = new ObjectReference[0]

ObjectReference[] LootArray = PlayerRef.FindAllReferencesOfType(kItemType, fRadius)

Int i = 0

While (i < LootArray.Length)k
	ObjectReference kItem = LootArray[i] as ObjectReference
	kResult.Add(kItem, 1)
	
	i += 1
EndWhile
```

When a script attempts to exceed the capacity of a dynamic array, Papyrus will log the following error:

> [error placeholder]

## Best practice

Check the length of the dynamic array and break the loop.

```
ObjectReference[] kResult = new ObjectReference[0]

ObjectReference[] LootArray = PlayerRef.FindAllReferencesOfType(kItemType, fRadius)

Int i = 0
Bool bBreak = False

While (i < LootArray.Length) && !bBreak
	If kResult.Length >= 128
		bBreak = True
	EndIf

	If !bBreak
		ObjectReference kItem = LootArray[i] as ObjectReference
		kResult.Add(kItem, 1)
	EndIf
	
	i += 1
EndWhile
```
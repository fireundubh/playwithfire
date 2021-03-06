---
title: Not validating the length of a dynamic array
description: 
published: true
date: 2020-01-20T12:13:38.074Z
tags: 
---

# Anti-pattern

A dynamic array is a new feature introduced by Fallout 4. Dynamic arrays can be created by passing zero to the array length. For example:

```
ObjectReference[] DynamicArray = new ObjectReference[0]
```

Unlike arrays returned by native functions and editor-filled array properties, dynamic arrays are limited to 128 items.

The author of the code below uses a loop to iterate through a native array and add items to a dynamic array without validating the length of the dynamic array.

```
ObjectReference[] DynamicArray = new ObjectReference[0]

ObjectReference[] NativeArray = PlayerRef.FindAllReferencesOfType(kItemType, fRadius)

Int i = 0

While i < NativeArray.Length
	ObjectReference kItem = NativeArray[i]
	DynamicArray.Add(kItem, 1)
	
	i += 1
EndWhile
```

When a script attempts to exceed the capacity of a dynamic array, Papyrus will log the following error:

> error: Array index 128 is out of range (0-127)

# Best practice

Check the length of the dynamic array and break the loop.

```
ObjectReference[] DynamicArray = new ObjectReference[0]

ObjectReference[] NativeArray = PlayerRef.FindAllReferencesOfType(kItemType, fRadius)

Int i = 0
Bool bBreak = False

While (i < NativeArray.Length) && !bBreak
	If DynamicArray.Length >= 128
		bBreak = True
	EndIf

	If !bBreak
		ObjectReference kItem = NativeArray[i]
		DynamicArray.Add(kItem, 1)
	EndIf
	
	i += 1
EndWhile
```
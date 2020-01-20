---
title: Not validating arrays before accessing array elements
description: 
published: true
date: 2020-01-20T12:08:24.137Z
tags: 
---

# Anti-pattern

The author of the code below attempts to access an element of an array without checking whether the array exists.

```
Int i = 0

While (i < ItemArray.Length)
	ObjectReference kItem = ItemArray[i] as ObjectReference
	
	; do stuff
	
	i += 1
EndWhile
```

If you try to access an element of a `None` array, Papyrus will log the following error:

> error: Cannot access an element of a `None` array

# Best practice

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

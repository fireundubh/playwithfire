---
title: Not validating objects or arguments before calling functions
description: 
published: true
date: 2020-01-20T12:11:55.094Z
tags: 
---

# Anti-pattern

The author of the code below calls a function without checking whether the arguments are correct.

```
; ObjectReference[] ItemArray = ...

Int i = 0

While i < ItemArray.Length
	ObjectReference kItem = ItemArray[i]
	
	kItem.Activate(DummyRef)
	
	i += 1
EndWhile
```

If an object or argument becomes `None` prior to the function call, Papyrus will abort the function call and log the following error:

> error: Cannot call `Activate()` on a `None` object, aborting function call

# Best practice

Check the variable or variables for `None` before the function call.

```
; ObjectReference[] ItemArray = ...

Int i = 0

While i < ItemArray.Length
	ObjectReference kItem = ItemArray[i]

	If kItem && DummyRef
		kItem.Activate(DummyRef)
	EndIf

	i += 1
EndWhile
```
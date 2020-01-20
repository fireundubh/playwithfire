---
title: Using multiple code paths in boolean functions
description: 
published: true
date: 2020-01-20T12:20:50.027Z
tags: 
---

# Anti-pattern

The author of the code below explicitly returns `True` and `False` in separate code paths for a boolean function.

```
Bool Function IsItemAvailable(ObjectReference akItem)
	If akItem.Is3DLoaded() && !akItem.IsDisabled() && !akItem.IsDeleted() && !akItem.IsDestroyed() && !akItem.IsActivationBlocked()
		Return True
	EndIf
	
	Return False
EndFunction
```

# Best practice

To avoid debugging multiple code paths, simplify the function.

```
Bool Function IsItemAvailable(ObjectReference akItem)
	Return akItem.Is3DLoaded() && !akItem.IsDisabled() && !akItem.IsDeleted() && !akItem.IsDestroyed() && !akItem.IsActivationBlocked()
EndFunction
```
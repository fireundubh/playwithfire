---
title: Not returning a value on all code paths
description: 
published: true
date: 2020-01-20T14:07:48.353Z
tags: 
---

# Anti-pattern

The author of the code below returns a value on two code paths, but the functon has three code paths.

```papyrus
Bool Function IsItemAvailable(ObjectReference akItem)
	If akItem.Is3DLoaded() && !akItem.IsDisabled() && !akItem.IsDeleted() && !akItem.IsDestroyed() && !akItem.IsActivationBlocked()
		Return True
	Else
		Return False
	EndIf
EndFunction
```

Papyrus raises a warning without an accompanying error:

> warning: Assigning `None` to an non-object variable named "`::temp21`"

# Best practice

Ensure that all code paths return a value. The above code could be written like so:

```papyrus
Bool Function IsItemAvailable(ObjectReference akItem)
	If akItem.Is3DLoaded() && !akItem.IsDisabled() && !akItem.IsDeleted() && !akItem.IsDestroyed() && !akItem.IsActivationBlocked()
		Return True
	EndIf
	
	Return False
EndFunction
```
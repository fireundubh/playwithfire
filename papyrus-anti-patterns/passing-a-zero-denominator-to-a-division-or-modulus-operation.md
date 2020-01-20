---
title: Passing a zero denominator to a division or modulus operation
description: 
published: true
date: 2020-01-20T12:15:49.575Z
tags: 
---

# Anti-pattern

The author of the code below attempts to divide a value by an actor value without checking whether the actor value is zero.

```
Actor Property PlayerRef Auto

Bool Function CanUnlock()
	Float fRatio = 100.0 / PlayerRef.GetActorValue("Lockpicking")

	If fRatio > 5.0
		Return True
	EndIf

	Return False
EndIf
```

Since an actor value (the denominator) can be zero, this function call may fail and Papyrus will log the following error:

> error: Cannot divide by zero

# Best practice

Check whether the denominator is zero and set the denominator to an acceptable nonzero value before executing a division or modulus operation.

```
Actor Property PlayerRef Auto

Bool Function CanUnlock()
	Float fSkill = PlayerRef.GetActorValue("Lockpicking")
	
	If fSkill == 0.0
		fSkill = 1.0
	EndIf
	
	Float fRatio = 100.0 / fSkill

	Return fRatio > 5.0
EndIf
```

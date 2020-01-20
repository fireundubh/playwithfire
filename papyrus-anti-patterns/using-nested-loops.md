---
title: Using nested loops
description: 
published: true
date: 2020-01-20T12:21:56.164Z
tags: 
---

# Anti-pattern

The author of the code below uses an outer loop and an inner loop to iterate over and process data in a list. In this example, the inner loop will execute on each item in the outer array.

```
Int i = 0

While i < DynamicArray.Length
	FormList kFormList = DynamicArray[i] as FormList
	
	Int j = 0
	Bool bBreak = False
	
	While (j < kFormList.GetSize()) && !bBreak
		If !bBreak
			ObjectReference kItem = kFormList.GetAt(j) as ObjectReference

			If kFormList.HasForm(kItem)
				; do stuff
				bBreak = True
			EndIf
		EndIf
		
		j += 1
	EndWhile
	
	i += 1
EndWhile
```

Assume there are 20 items in `DynamicArray` and 20 items in each `kFormList`:

- If the inner loop condition is met on the first iteration, these nested loops would iterate 40 times.
- If the inner loop condition is never met, these nested loops would iterate 420 times.

How many iterations would be needed to complete three, or four, or five nested loops?

# Best practice

Consider whether you need to access every value in each loop. If nested loops are the correct solution, look closer at where you can optimize.

Otherwise, always finish your code as fast as possible. Using properties, the above code can be refactored like so:

```
FormList Property MyFormList1 Auto Const
FormList Property MyFormList2 Auto Const

Int i = 0
Bool bBreak = False

While (i < DynamicArray.Length) && !bBreak
	If !bBreak
		ObjectReference kItem = DynamicArray[i]
	
		If MyFormList1.HasForm(kItem)
			; do stuff
			bBreak = True
		EndIf
	
		If MyFormList2.HasForm(kItem)
			; do stuff
			bBreak = True
		EndIf
	EndIf
	
	i += 1
EndWhile
```
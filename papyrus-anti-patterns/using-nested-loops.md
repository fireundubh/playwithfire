<!-- TITLE: Using nested loops -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Using nested loops
## Anti-pattern

The author of the code below uses an outer loop and an inner loop to iterate over and process data. In this example, the inner loop will execute on each item in the outer array.

> **Editorial Note:** For the sake of clarity, some best practices are ignored in this example.

```
Int i = 0

While (i < outerArray.Length)
	ObjectReference kItem = outerArray[i] as ObjectReference
	
	Int j = 0
	
	While (j < innerArray.Length)
		Formlist kFormlist = innerArray[j] as Formlist
		
		If kFormlist.HasForm(kItem)
			; do stuff
		EndIf
		
		j += 1
	EndWhile
	
	i += 1
EndWhile
```

## Best practice

Always finish your code as fast as possible. The above code can be refactored like so:

```
Formlist Property myFormlist1 Auto Const
Formlist Property myFormlist2 Auto Const

Int i = 0
Bool bBreak = False

While (i < outerArray.Length) && !bBreak
	If !bBreak
		ObjectReference kItem = outerArray[i] as ObjectReference
	
		If myFormlist1.HasForm(kItem)
			; do stuff
			bBreak = True
		EndIf
	
		If myFormlist2.HasForm(kItem)
			; do stuff
			bBreak = True
		EndIf
	EndIf
	
	i += 1
EndWhile
```

<!-- TITLE: Using compound conditional statements instead of logic gates -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Using a compound conditional statement instead of logic gates
## Anti-pattern

The author of the code below constructed a compound conditional statement to control the flow of this function.

```
Bool Function IsItemDeletedDisabledOrDestroyed(ObjectReference akItem)
	If akItem.IsDisabled() || akItem.IsDeleted() || akItem.IsDestroyed()
		Return True
	EndIf

	Return False
EndFunction
```

## Best practice

To improve maintainability, use logic gates instead of compound conditional statements.

```
Bool Function IsItemDeletedDisabledOrDestroyed(ObjectReference akItem)
	If akItem.IsDisabled()
		Return True
	EndIf
	
	If akItem.IsDeleted()
		Return True
	EndIf
	
	If akItem.IsDestroyed()
		Return True
	EndIf

	Return False
EndFunction
```

<!-- TITLE: Not using a break condition in a loop -->

# Not using a break condition in a loop
## Anti-pattern

The author of the code below uses a loop to iterate through an array unconditionally. The loop completes after reaching the last item in the array.

```
Int i = 0

While (i < NativeArray.Length)
	If PlayerRef.WouldBeStealing(objLoot)
		objLoot.SetActorRefOwner(PlayerRef)
	EndIf
	
	i += 1
EndWhile
```

## Best practice

Loops should be able to terminate prematurely when a condition arises where exiting is the only safe action.

> **Developer Note:** "While loops  keep the thread alive, which consumes some memory, as the thread and all its stack data and calling functions stack data need to stick around. If you end up with >100 threads running at once for over a few seconds, Papyrus assumes something is wrong and starts spitting out stack dumps to the log so you can find and fix the problem. If the while loops aren't sleeping (via Wait or some other latent call) they can contribute to script lag as the VM has to take time to process the thread in addition to everything else it's running." —SmkViper

In the absence of formal `break` statements, the code above could be written:

```
Int i = 0
Bool bBreak = False

While (i < NativeArray.Length) && !bBreak
	If !GameStateIsValid()
		bBreak = True
	EndIf
	
	If !bBreak
		If PlayerRef.WouldBeStealing(objLoot)
			objLoot.SetActorRefOwner(PlayerRef)
		EndIf
	EndIf
	
	i += 1
EndWhile
```
---
title: Not returning a value on all code paths
description: 
published: true
date: 2020-11-29T10:59:17.604Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:07:22.950Z
---

# Anti-pattern

The author of the code below returns a value on two code paths, but the functon has three code paths.

```papyrus
Bool Function IsRefNotLoaded(ObjectReference akRef)
	If akRef.Is3DLoaded()
  	Return False
  EndIf
EndFunction
```

Papyrus raises a warning without an accompanying error:

> warning: Assigning `None` to an non-object variable named "`::temp21`"

# Best practice

Ensure all code paths return a value. The above code could be written like so:

```papyrus
Bool Function IsRefNotLoaded(ObjectReference akRef)
	If akRef.Is3DLoaded()
  	Return False
  EndIf
  
  Return True
EndFunction
```

We can also condense the function body to a single line:

```papyrus
Bool Function IsRefNotLoaded(ObjectReference akRef)
	Return !akRef.Is3DLoaded()
EndFunction
```
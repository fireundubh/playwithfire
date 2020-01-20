---
title: Using a single letter to name your variables
description: 
published: true
date: 2020-01-20T12:19:00.011Z
tags: 
---

# Anti-pattern

Sometimes programmers will use single letters to name variables. This produces unreadable and hard-to-maintain code.

```
GlobalVariable Property c Auto Const

Float Function gbsw(Float a)
	Float b = gbs()
	
	If b > 100.0
		b = 100.0
	EndIf
	
	Return Math.Floor(((c.GetValue() * b) / 100.0) * a)
EndFunction
```

# Best practice

The compiler does not care if you call a variable `a` or `abracadabra`. Variables should be named to help the programmer.

```
GlobalVariable Property BestSkillContribMax Auto Const

Float Function GetBestSkillWeight(Float afSkillPenalty)
	Float fBestSkill = GetBestSkill()
	
	If fBestSkill > 100.0
		fBestSkill = 100.0
	EndIf
	
	Return Math.Floor(((BestSkillContribMax.GetValue() * fBestSkill) / 100.0) * afSkillPenalty)
EndFunction
```

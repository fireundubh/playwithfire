<!-- TITLE: Using a single letter to name your variables -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Using a single letter to name your variables
## Anti-pattern

Sometimes programmers will use single letters to name variables. This produces unreadable and hard-to-maintain code.

```
GlobalVariable Property c Auto Const

Float Function GetBestSkillWeight(Float a)
	Float b = GetBestSkill()
	
	If b > 100
		b = 100
	EndIf
	
	Return ((c.Value * b) / 100) * a
EndFunction
```

## Best practice

The compiler does not care if you call a variable `a` or `abracadabra`. Variables should be named to help the programmer.

```
GlobalVariable Property fBestSkillContribMax Auto Const

Float Function GetBestSkillWeight(Float afSkillPenalty)
	Float fBestSkill = GetBestSkill()
	
	If fBestSkill > 100
		fBestSkill = 100
	EndIf
	
	Return ((fBestSkillContribMax.Value * fBestSkill) / 100) * afSkillPenalty
EndFunction
```

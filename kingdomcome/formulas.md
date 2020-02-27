---
title: Known Formulas
description: 
published: true
date: 2020-02-27T08:18:19.365Z
tags: 
---

For the default values of RPG parameters, refer to the [RPG Parameters](https://wiki.fireundubh.com/kingdomcome/rpg-parameters) page.

# Gameplay

## Amount of dirty add

```lua
dirtAdded = DerivStat_ClothDirtyingSpeedKm * distanceTraveled / 1000
```

## Speed of dirt accumulation

```lua
DerivStat_ClothDirtyingSpeedKm =
	1000 / lerp(RPG.FullClothDirtyingOnZeroSpeed, RPG.FullClothDirtyingOnFullSpeed, surface.movementSpeedMult)
```

**Note:** `surface.movementSpeedMult` is defined in `gamedata.pak\Libs\MaterialEffects\SurfaceTypes.xml`.

## Perk points per stat/skill

```lua
perkPointCount = min(
	(perkCount <= RPG.MinPerkPoints ? perkCount : perkCount - RPG.MinLeftoverPerks),
  RPG.MaxPerkPoints
)
```

# Herbalism

## Amount of collected herbs

```lua
numOfHerbs = RPG.HerbGatherSkillToCount * sqrt(skillLevel)
```

## Radius of herb collection

```lua
radius = RPG.HerbGatherSkillToRadius * skillLevel
```

# Lockpicking

## Lockpicking tolerance

```lua
computedTolerance = 
	RPG.LockPickingToleranceMCoef
	- (RPG.LockPickingToleranceNCoef * difficultyModifier) 
	- ((RPG.LockPickingToleranceACoef * e) ^ (-RPG.LockPickingToleranceKCoef * skill))
```

## XP reward for picking locks

```lua
XP = RPG.LockPickingSuccessXPMulCoef * (lockDifficulty + 1) / (RPG.LockPickingSuccessXPDivCoef * skillLevel + 1)
```

## Stealth XP reward for picking locks

```lua
XP = bWasLockPicked ? RPG.LockPickingStealthXP : nil
```

# Well Worn Perk

## Equipment weight after reduction

```lua
equippedWeight = standardWeight * (1.0 - RPG.EquippedWeightSubWithWellWornPerk)
```
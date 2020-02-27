---
title: Known Formulas
description: 
published: true
date: 2020-02-27T08:15:24.294Z
tags: 
---

For the default values of RPG parameters, refer to the [RPG Parameters](https://wiki.fireundubh.com/kingdomcome/rpg-parameters) page.

# Gameplay

## Dirt Added

```lua
dirtAdded = DerivStat_ClothDirtyingSpeedKm * distanceTraveled / 1000
```

## Cloth Dirtying Speed

```lua
DerivStat_ClothDirtyingSpeedKm =
	1000 / lerp(FullClothDirtyingOnZeroSpeed, FullClothDirtyingOnFullSpeed, surface.movementSpeedMult)
```

**Note:** `surface.movementSpeedMult` is defined in `gamedata.pak\Libs\MaterialEffects\SurfaceTypes.xml`.

## Perk Points per Stat/Skill

```lua
perkPointCount = min(
	(perkCount <= RPG.MinPerkPoints ? perkCount : perkCount - RPG.MinLeftoverPerks),
  RPG.MaxPerkPoints
)
```

# Herbalism

## Number of Collected Herbs

```lua
numOfHerbs = RPG.HerbGatherSkillToCount * sqrt(skillLevel)
```

## Radius of Herb Collection

```lua
radius = RPG.HerbGatherSkillToRadius * skillLevel
```

# Lockpicking

## Lockpicking Tolerance

```lua
computedTolerance = 
	LockPickingToleranceMCoef
	- (LockPickingToleranceNCoef * difficultyModifier) 
	- ((LockPickingToleranceACoef * e) ^ (-LockPickingToleranceKCoef * skill))
```

## XP Reward for Picking Locks

```lua
XP = RPG.LockPickingSuccessXPMulCoef * (lockDifficulty + 1) / (RPG.LockPickingSuccessXPDivCoef * skillLevel + 1)
```

## Stealth XP Reward for Picking Locks

```lua
XP = bWasLockPicked ? RPG.LockPickingStealthXP : nil
```

# Well Worn Perk

## Weight Reduction

```lua
equippedWeight = standardWeight * (1.0 - RPG.EquippedWeightSubWithWellWornPerk)
```
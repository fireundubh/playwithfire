---
title: Known Formulas
description: 
published: true
date: 2020-02-27T08:40:35.413Z
tags: 
---

For the default values of RPG parameters, refer to the [RPG Parameters](https://wiki.fireundubh.com/kingdomcome/rpg-parameters) page.

# Gameplay

## Speed of dirt accumulation

This is the formula for the derived stat `DerivStat_ClothDirtyingSpeedKm`.

```lua
return 1000 / lerp(RPG.FullClothDirtyingOnZeroSpeed, RPG.FullClothDirtyingOnFullSpeed, surface.movementSpeedMult)
```

**Note:** `surface.movementSpeedMult` is defined in `gamedata.pak\Libs\MaterialEffects\SurfaceTypes.xml`.

## Amount of dirt to accumulate

```lua
return DerivStat_ClothDirtyingSpeedKm * distanceTraveled / 1000
```

## Perk points per stat/skill

```lua
if perkCount <= RPG.MinPerkPoints then
	return min(perkCount, RPG.MaxPerkPoints)
end

return min(perkCount - RPG.MinLeftoverPerks, RPG.MaxPerkPoints)
```

# Herbalism Skill

## Amount of collected herbs

```lua
return RPG.HerbGatherSkillToCount * sqrt(skillLevel)
```

## Radius of herb collection

```lua
return RPG.HerbGatherSkillToRadius * skillLevel
```

# Lockpicking Skill

## Lockpicking tolerance

Tolerance is unrelated to minigame difficulty. If `computedTolerance > appropriateTolerance`, the lock is considered too hard to pick and the minigame will not start. Since 2018, the game displays a "too hard to pick" notification when this condition is `true`. If the values of `RPG.LockPickingAppropriateTolerance` and/or `RPG.ControllerLockPickingAppropriateTolerance` are negative, this condition will always be `false`, allowing the player to start the minigame for locks beyond the player's skill level.

```lua
M = RPG.LockPickingToleranceMCoef
N = RPG.LockPickingToleranceNCoef
A = RPG.LockPickingToleranceACoef
K = RPG.LockPickingToleranceKCoef

computedTolerance = M - N * difficultyModifier - A * e ^ (-K * skill)

-- clamp computed tolerance between 0 and 1
if computedTolerance < 0 then
	return 0
end

if computedTolerance > 1 then
	return 1
end

return computedTolerance
```

**Note:** The computed tolerance is clamped between 0 and 1.

## XP reward for picking locks

```lua
XPMulCoef = RPG.LockPickingSuccessXPMulCoef
XPDivCoef = RPG.LockPickingSuccessXPDivCoef

return XPMulCoef * (lockDifficulty + 1) / (XPDivCoef * skillLevel + 1)
```

## Stealth XP reward for picking locks

```lua
if bWasLockedPicked then
	return RPG.LockPickingStealthXP
end

return nil
```

# Well Worn Perk

## Equipment weight after reduction

```lua
return standardWeight * (1.0 - RPG.EquippedWeightSubWithWellWornPerk)
```
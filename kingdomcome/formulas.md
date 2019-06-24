<!-- TITLE: Known Formulas -->

# Known Formulas
## Table

Category| Description | Formula
--- | --- | ---
Gameplay | Dirt added | `dirtAdded = DerivStat_ClothDirtyingSpeedKm * distanceTraveled / 1000`
Gameplay | DerivStat_ClothDirtyingSpeedKm | `DerivStat_ClothDirtyingSpeedKm = 1000 / lerp(FullClothDirtyingOnZeroSpeed, FullClothDirtyingOnFullSpeed, surface.movementSpeedMult)`
Gameplay | Perk points per stat/skill | `perkPointCount = min((perkCount <= RPG.MinPerkPoints ? perkCount : perkCount - RPG.MinLeftoverPerks), RPG.MaxPerkPoints)`
Herbalism Skill | Number of collected herbs | `numOfHerbs = RPG.HerbGatherSkillToCount * sqrt(skillLevel)`
Herbalism Skill | Radius of herb collection | `radius = RPG.HerbGatherSkillToRadius * skillLevel`
Lockpicking Skill | XP reward for picking locks | `XP = RPG.LockPickingSuccessXPMulCoef * (lockDifficulty + 1) / (RPG.LockPickingSuccessXPDivCoef * skillLevel + 1)`
Lockpicking Skill | Stealth XP reward for picking locks | `XP = bWasLockPicked ? RPG.LockPickingStealthXP : nil`
Well Worn Perk | Weight reduced by Well Worn perk | `equippedWeight = standardWeight * (1.0 - RPG.EquippedWeightSubWithWellWornPerk)`

For the default values of RPG parameters, refer to the [RPG Parameters](https://wiki.fireundubh.com/kingdomcome/rpg-parameters) page.

### Notes

`surface.movementSpeedMult` is defined in `gamedata.pak\Libs\MaterialEffects\SurfaceTypes.xml`.
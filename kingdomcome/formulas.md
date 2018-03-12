<!-- TITLE: Known Formulas -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Known Formulas
## Table

Category| Description | Formula
--- | --- | ---
Gameplay | Perk points per stat/skill | `perkPointCount = min((perkCount <= RPG.MinPerkPoints ? perkCount : perkCount - RPG.MinLeftoverPerks), RPG.MaxPerkPoints)`
Herbalism Skill | Number of collected herbs | `numOfHerbs = RPG.HerbGatherSkillToCount * sqrt(skillLevel`
Herbalism Skill | Radius of herb collection | `radius = RPG.HerbGatherSkillToRadius * skillLevel`
Lockpicking Skill | XP reward for picking locks | `XP = RPG.LockPickingSuccessXPMulCoef * (lockDifficulty + 1) / (RPG.LockPickingSuccessXPDivCoef * skillLevel + 1)`
Well Worn Perk | Weight reduced by Well Worn perk | `equippedWeight = standardWeight * (1.0 - EquippedWeightSubWithWellWornPerk)`

For default values of RPG parameters, refer to the [RPG Parameters](https://wiki.fireundubh.com/kingdomcome/rpg-parameters) page.
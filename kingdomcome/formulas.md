<!-- TITLE: Known Formulas -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Known Formulas
## Table

Description | Formula
--- | ---
Perk points per stat/skill | `perkPointCount = min((perkCount <= RPG.MinPerkPoints ? perkCount : perkCount - RPG.MinLeftoverPerks), RPG.MaxPerkPoints)`
Weight reduced by Well Worn perk | `equippedWeight = standardWeight * (1.0 - EquippedWeightSubWithWellWornPerk)`
XP reward for picking locks | `XP = RPG.LockPickingSuccessXPMulCoef * (lockDifficulty + 1) / (RPG.LockPickingSuccessXPDivCoef * skillLevel + 1)`

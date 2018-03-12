<!-- TITLE: Known Formulas -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Known Formulas
## Table

Description | Formula
--- | ---
Total perk points per stat/skill | `perkPointCount = min((perkCount <= RPG.MinPerkPoints ? perkCount : perkCount - RPG.MinLeftoverPerks), RPG.MaxPerkPoints)`
XP reward for picking locks | `RPG.LockPickingSuccessXPMulCoef * (lockDifficulty + 1) / (RPG.LockPickingSuccessXPDivCoef * skillLevel + 1)`

---
title: Master of Disguise
description: 
published: true
date: 2021-03-20T02:25:13.161Z
tags: 
editor: markdown
dateCreated: 2021-03-20T02:22:08.866Z
---

> [Version History (SSE)](/mods/master-of-disguise/version-history) &bull; [Frequently Asked Questions](/mods/master-of-disguise/faqs)
{.is-info}

# Overview

**Master of Disguise** transforms faction armor into real disguises with an immersive and fully customizable detection system.

* Suit up as anyone, from a Dark Brotherhood assassin to a rough-and-tumble bandit.
* Find safety among new allies, or deceive and betray them.
* Wage war against new enemies, or fire the first shot.

You are the Master of Disguise. What will you do?


# Accolades

* [Featured by GameSpot](http://www.gamespot.com/videos/top-5-skyrim-mods-of-the-week-become-the-master-of/2300-6423174/) ([@8:11](https://www.youtube.com/watch?v=QZxRm1EcbQ4&t=8m11s))
* [Featured by Kotaku](http://kotaku.com/skyrim-disguises-let-you-walk-around-doing-whatever-1681784966)
* [Featured by MxR Mods](https://youtu.be/69e7xcYw-G4?t=2m48s) ([@2:48](https://youtu.be/69e7xcYw-G4?t=2m48s))
* [Featured by Brodual](https://www.youtube.com/watch?v=ATGNFDgNT-A)
* [Featured by Pandapa](https://www.youtube.com/watch?v=wwWXKB9rol4)
* #1 in Stealth in the Skyrim G.E.M.S. Hall of Fame (pre-GitHub)
* #1 in Stealth on the Skyrim Nexus (pre-GitHub)
* 9.7/10 on the Steam Workshop (pre-GitHub)


# Requirements

* Skyrim Special Edition v1.5.39
* SkyUI and SKSE (only for SkyUI MCM support)


# Avoiding Detection

NPCs now have a horizontal front-facing field of view, or cone of vision, that extends outward up to a predetermined distance. The fDetectionViewCone game setting, changed or dynamically adjusted by some mods, determines the width of the cone, and the amount of light on the player adjusts the distances at which NPCs can recognize the player.

Periodically, while the player is within that cone of vision, NPCs may become suspicious. If an NPC becomes suspicious, the player will be notified that "you are being watched" in the top left corner of the screen. The identity of the suspicious NPC will not be revealed; however, the player will have seconds to lose their line of sight, which, in addition to cover, can also be achieved by moving into dark or dimly lit areas of the geography.

If the player fails to lose their line of sight, the player and NPC will make dice rolls to determine whether the NPC discovers the player. If the player wins the dice roll, life will go on and nobody will be any wiser. If the player loses the dice roll, combat will begin, but only if the NPC would have been hostile normally.

# NPC Perception Model

## Field of View Segmentation

Clear | Distorted | Peripheral
:--- | :--- | :---
-15° to 15° | -30° to -15° and 15° to 30° | -60° to -30° and 30° to 60°


## Line of Sight Ranges

* The ranges 512, 1024, and 2048 are dynamically adjusted by light level.
* The base LOS distance max is configurable by the player.
* Adjustment formula: `fLOSDistanceMaxBase x (fLightLevel / 100.0)`
* Default Value: `fLOSDistanceMaxBase = 2048.0`

## Line of Sight Penalties

* When rolling for discovery, the player's skill contribution to the dice roll is multiplied by a skill penalty determined by where the player was suspected in the cone of vision.
* For example, if the player's adjusted skill score was 50, that score would be multiplied by 0.75, 0.8, or 0.85, so the effective skill score would be respectively 37.5, 40, or 42.5.
* Originally, there were more penalties, as indicated in the graphic, but the gain did not justify the complexity.
* Skill formula: `((fBestSkillContribMax x fSneakOrIllusionOrSpeechSkill) / 100.0) x fSkillPenalty`
* Default Value: `fBestSkillContribMax = 50.0`


# Rolling for Discovery

The player's skill in Sneak, Illusion, or Speech, behaviors, race, and disguise coverage are combined into a "identity score" that is rolled against a random number between 0 and 99. If the identity score is greater than the random number, the player wins the discovery roll and the NPC will not become hostile.

## Racial Synergies

Skyrim factions respond differently to the Man, Mer, and Beast races. Master of Disguise takes those biases into account:

Race | Faction | Modifier
:--- | :--- | :---
All | Daedra | Penalty
Altmer | Bandits | Penalty
Altmer | Stormcloaks | Penalty
Altmer | Thalmor | Bonus
Altmer | Windhelm Guard | Penalty
Argonian | Thieves Guild | Bonus
Bosmer | Thalmor | Bonus
Breton | Forsworn | Bonus
Breton | Markarth Guard | Penalty
Dunmer | Cultists | Bonus
Dunmer | Morag Tong | Bonus
Dunmer | Redoran Guard | Bonus
Imperial | Blades | Bonus
Imperial | Imperial Legion | Bonus
Imperial | Penitus Oculatus | Bonus
Imperial | Solitude Guard | Bonus
Imperial | Stormcloaks | Penalty
Khajiit | Thieves Guild | Bonus
Nord | Cultists | Bonus
Nord | Markarth Guard | Bonus
Nord | Solitude Guard | Penalty
Nord | Stormcloaks | Bonus
Nord | Windhelm Guard | Bonus
Orc | Imperial Legion | Bonus
Orc | Penitus Oculatus | Bonus
Orc | Solitude Guard | Bonus
Redguard | Alik'r Mercenaries | Bonus
Vampire | Clan Volkihar | Bonus
Vampire | Dark Brotherhood | Bonus
Vampire | Dawnguard | Penalty
Vampire | Necromancers | Bonus
Vampire | Vampires | Bonus
Vampire | Vigil of Stendarr | Penalty
All Others | Alik'r Mercenaries | Penalty
All Others | Bandits | Bonus
All Others | Forsworn | Penalty
All Others | Thalmor | Penalty

## Leaving Witnesses

If a faction NPC is attacked by the player in disguise, the player will be immediately discovered and attacked. If the NPC is dispatched without any witnesses nearby, the player's disguise will be restored.

## Escaping

When the player is discovered, it is not necessary to engage in combat, although hostilities will begin. If the player is able to outpace the pursuers by some distance, they will give up the chase and return to their patrol points. Although requiring some suspension of disbelief, this allows the player to try again without reloading a save.

## Factions

Disguises not only deceive members of the factions to whom the disguise belongs but also enemies of those factions. Opposing factions, which may not normally be hostile to the player, may see the player as an enemy.

In addition, faction NPCs engaged in combat with other NPCs, except companions, will not roll for discovery.


# SkyUI Mod Configuration Menu

Using the new SkyUI Mod Configuration Menu, the player can adjust nearly every aspect of the discovery system from within the game. The disguise and discovery systems can be toggled independently as well.

## Example: Scoring Menu

![Scoring Menu](https://camo.githubusercontent.com/d966d3c9d2d0f2a04f5398a9831f99f66d26c2e1/687474703a2f2f692e696d6775722e636f6d2f6a685a515652762e6a7067)

## Example: Crime Menu

![Crime Menu](https://camo.githubusercontent.com/b7fba3732f972e4e251858e4972cedf36d2673e5/687474703a2f2f692e696d6775722e636f6d2f4469537471424e2e6a7067)


# How to Wear a Disguise

To wear most disguises, the player will need to equip faction armor in only the body slot. Some disguises have special requirements. However, the disguise will be always more effective when complete.

## Special Requirements

> **Tip:** Items that satisfy these requirements can be found on the respective faction members.
{.is-info}

* The player must wear the Ring of the Silver Hand to infiltrate the Silver Hand.
* The player must wear the Vigilant's Amulet of Stendarr to infiltrate the Vigil of Stendarr.
* The player must equip the Eastmarch Guard's Shield to infiltrate the Windhelm Guard. The Windhelm Guard wear regular Stormcloak uniforms and have only this shield to separate them.
* Dragonborn: The player must wear the Cultist Mask to infiltrate Miraak's Cultists.

## Priority Rule

Only the first disguise equipped will be activated. You will need to unequip that disguise to switch to another.


# Unique Disguise Behaviors

## Bandit Disguises

> This feature can be toggled from the SkyUI Mod Configuration Menu.
{.is-info}

> The slot checked when determining whether to activate this disguise can be changed in the Crime menu.
{.is-info}

The player can wear a bandit disguise comprised of:

- Fur Armor
- Fur Helmet
- Fur Bracers, or Fur Gauntlets (found on Stormcloaks)
- Fur Shoes, or Fur Boots (found on Stormcloaks)

All hold guards are hostile to bandits.

## Daedric Weapons and Armor

> This feature can be toggled from the SkyUI Mod Configuration Menu.
{.is-info}

"The Mercy of Stendarr does not extend to Daedra worshippers." — The Vigil of Stendarr

When the player equips Daedric weapons or armor, Vigilants will attempt to drag the player into the light.

In addition, Dremora will see the player as aligned with Mehrunes Dagon and will not attack.

## Guard Disguises

> Currently not available in any version.
{.is-warning}

When the player equips a guard disguise, the player's bounty is concealed in the respective hold. For example, wearing the Windhelm Guard disguise will conceal the player's bounty in Eastmarch but not The Reach.

In addition, the amount of the bounty will be used to determine the effectiveness of the disguise. By default, the player can achieve 50% effectiveness at 1,000 septims, which is the default bounty for murder.

While in a guard disguise, if the player commits a crime and leaves witnesses, the player will incur a bounty and the disguise will no longer have the desired effect. But smaller bounties can still be paid off.

When the player is discovered, or the disguise is no longer worn, the player's active bounty will be restored. Any bounties incurred while in the disguise will be added to the player's active bounty.

**Known Exploit:** The player can continually re-equip the guard disguise to continually conceal the active bounty, and effectively commit most crimes without penalties while in disguise. However, the tracked bounty will continue to increase, so at some point, the player will have to address the enlarged active bounty.

## Vampire Disguises

> This feature can be toggled from the SkyUI Mod Configuration Menu.
{.is-info}

Vampire disguises can be worn at any time, but using the Mod Configuration Menu, you can configure vampire disguises to obey the day/night cycle.

If that option is enabled, vampire disguises cannot be used during the day and will deactivate after night passes.

## Werewolf Disguises

> This feature can be toggled from the SkyUI Mod Configuration Menu.
{.is-info}

Wearing the Savior's Hide, a gift from Hircine, will signal to Werewolves that the player is favored and the player will not be attacked by Werewolves.


# Compatibility

## Guidelines

* Hard incompatibility with mods that add or remove the player from base factions
* Hard incompatibility with mods that offer similar features
* *New* faction equipment added by mods cannot be used as disguise equipment without patches.
* Custom races will not have any racial bonuses or penalties when your dice roll is calculated.

## Incompatible Mods

Version | Mod | Reason
:--- | :--- | :---
LE | Armor Disguises | Breaks the game by adding and removing the player from base factions
LE | Skyrim Redone (SkyRe) | Similar features but less featureful
LE | PerMa | Similar features but less featureful


# Uninstalling

Bethesda Softworks does not support uninstalling mods. Loading saves without previously active mods may break those saves.
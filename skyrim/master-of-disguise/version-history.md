---
title: Version History
description: 
published: true
date: 2020-03-04T23:07:55.154Z
tags: 
---

# Version 1.4.1

- A setting has been added to the Advanced menu that allows you to disable automatic faction updates (i.e., Factions Update Auto Run.) After updating once, you can toggle this setting, save, and when loading that save, you will not see the update message box again.

**Important:** If you later install mods that change faction relationships, or if faction NPCs are ignoring your disguise, you should re-enable this setting, save, and reload that save to update faction relations again.

- Your Speech(craft) skill is now considered when calculating your skill score and its weight on the effectiveness of your disguise.

# Version 1.4

## Requirements Changes

- Minimum game version: Skyrim Special Edition v1.5.39.0
- Removed master/dependency: Unofficial Skyrim Special Edition Patch

## Major Changes

- When changing disguises, those disguises will activate in significantly less time than previous versions.
- When starting a new game or loading a save, faction relationships will automatically update. The faction relationships overhaul, which caused Civil War issues for some players, has been removed.
- By default, changing disguises will show faction notifications as message boxes. The display mode can be toggled in Advanced settings.
- By default, the Bandit disguise is disabled. The disguise can be toggled in Crime settings.
- By default, the Vampire disguise day/night restrictions are disabled. This feature can be toggled in Discovery settings.

## Fixes

- Fixed issue where hair and circlet scores could be counted incorrectly
- Fixed issue where more than one disguise could be enabled at a time
- Fixed issue where equipping/unequipping disguises while in combat could produce out-of-sync behavior
- Fixed issue where faction relationships could not be changed by plugin if they were baked into saves
- Fixed issue where some default values were incorrect which trivialized avoiding discovery
- Fixed issue where equipping disguises before tutorial chain completed could repeat tutorial messages
- Fixed issue where delay between dice roll attempts was set too low by default
- Fixed issue where disguises sharing items were not activated correctly (e.g., Bandit, Silver Hand, Stormcloaks)
- Fixed issue where Bandit Disguise essential slot could not be configured from SkyUI menu
- Fixed issue where Daedric Influence was activated only when Daedric headwear was equipped
- Fixed issue where script performance would suffer during combat with effects that trigger multiple OnHit events
- Fixed various issues where SkyUI menu help descriptions were inaccurate or outdated
- Fixed various issues with states and persistent reference locks

## Debugging

- Implemented cheat menu for adding faction equipment
- Increased max update rate for monitor script to 30 seconds
- Enabled Papyrus logging by default
- Consolidated logging options in SkyUI menu
- Added severity prefixes to log messages
- Added more log messages

## Maintenance

- Refactored, reorganized, and removed obsolete code
- Removed unused strings from English localization
- Packaged logo texture into separate BSA


# Version 1.3

- Added support for SkyUI Mod Configuration Menu (requires SKSE and SkyUI)
- Added option to force vampire disguises to obey day/night cycle (enabled by default)
- Significantly improved performance and responsiveness of equipping and unequipping disguises
- Fixed issue where a player alias pointed to the wrong player address
- Forwarded faction relationship fix from Unofficial Skyrim Special Edition Patch
- Updated English translation for SkyUI Mod Configuration Menu


# Version 1.2

- Fixed the issue preventing the detection system from working
- Disabled debug logging because some people still believe the Papyrus log helps solve crashes
- Cleaned up unused code
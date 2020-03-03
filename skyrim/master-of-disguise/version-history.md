---
title: Version History
description: 
published: true
date: 2020-03-03T23:54:18.153Z
tags: 
---

# Version 1.4 (Unreleased)

## TODO

After this list of unimplemented changes is complete, they will be recorded properly and the next version will be released.

- [ ] When the player equips or unequips a disguise, the player should be prompted instead of notified. We want to avoid players being confused about when they're disguised; notifications may not call enough attention to themselves.
- [ ] The player should be able to choose whether to see notifications or prompts, but prompts will be the new default.
- [ ] The player should be prompted when the initial faction relationships update has started and when that update has completed. We want to signal to the player when the disguise mechanic is ready. Currently, the update is silent, and if the player tries to use disguises during the update process, factions may not be updated and disguises will not behave as expected.

## Requirements Changes

- Minimum game version: Skyrim Special Edition v1.5.39.0
- Removed master/dependency: Unofficial Skyrim Special Edition Patch

## Major Changes

- Significantly reduced time to activate disguises when changing equipment
- Updated critical faction relationships programmatically when starting a new game or loading a save
- Removed faction relationships overhaul, eliminating any need for the Joinable Factions Patch
- Disabled Bandit Disguise by default
- Disabled Vampire Disguise day/night restrictions by default
- Added developer message to tutorial message chain

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
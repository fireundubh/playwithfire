---
title: Version History
description: 
published: true
date: 2020-01-31T00:36:40.574Z
tags: 
---

# Version 1.4 (Unreleased)

Minimum game version required: Skyrim Special Edition v1.5.39.0

## Major Changes

- Significantly reduced time to activate disguises when changing equipment
- Updated critical faction relationships programmatically when starting a new game or loading a save
- Removed faction relationships overhaul, eliminating any need for the Joinable Factions Patch
- Disabled Bandit Disguise by default
- Disabled Vampire Disguise day/night restrictions by default
- Added developer message to tutorial message chain

## Fixes

- Fixed issue where faction relationships could not be changed by plugin if they were baked into saves
- Fixed issue where some default values were incorrect which trivialized avoiding discovery
- Fixed issue where equipping disguises before tutorial chain completed could repeat tutorial messages
- Fixed issue where delay between dice roll attempts was set too low by default
- Fixed issue where disguises sharing items were not activated correctly (e.g., Bandit, Silver Hand, Stormcloaks)
- Fixed issue where Bandit Disguise essential slot could not be configured from SkyUI menu
- Fixed issue where Daedric Influence was activated only when Daedric headwear was equipped
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
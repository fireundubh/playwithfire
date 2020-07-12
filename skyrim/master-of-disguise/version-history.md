---
title: Version History
description: 
published: true
date: 2020-07-12T09:55:07.867Z
tags: 
editor: markdown
---

# Version 1.5.0 (in development)

## Requirements Changes

Master of Disguise SSE v1.5 requires SKSE.

> &bull; Skyrim Special Edition v1.5.39.0 is no longer the required minimum game version.
> &bull; Individual slot formlists are no longer required for extension patches.
{.is-warning}

## Major Changes

### Initialization

> In v1.4, Master of Disguise removed direct faction edits and introduced a faction relations updater to set up disguises at runtime, in exchange for greater intermod compatibility. Unfortunately, nearly 500 calls to the `SetAlly` and `SetEnemy` functions were required, and that many calls carried a significant initialization time penalty.
{.is-info}

In v1.5, the time to complete updating faction relations has been significantly reduced. Instead of updating *all* factions at once, only faction relations relevant to a disguise will be updated when that disguise is equipped. This update will occur only once per disguise in a playthrough.

To be clear, the faction relations updater has not been removed but now only updates faction relations for intermod compatibility. Furthermore, because there are few such relations that need to be updated at this stage, players will no longer be prompted.

### Rules

- Only one disguise can be active at any time
- Restored Field of View penalties (clear, distorted, peripheral)
- Field of View and Line of Sight penalties affect NPC dice roll, instead of player skill weight
- MCM: Added Line of Sight penalties (mid, far)
- MCM: Renamed Field of View and Line of Sight headings accordingly

### Performance

- Increased rate at which disguises are detected when equipped and unequipped
- Increased rate at which equipment weight on discovery roll is calculated
- Increased rate at which race weight on discovery roll is calculated
- Increased rate at which damage sources are checked against excluded damage sources formlist

### Localization

- Added localization support (`.STRINGS`, `.DLSTRINGS`, `.ILSTRINGS`)

## Fixes

- Fixed issue where some disguises could not deactivate
- Fixed issue where the Bandit and Silver Hand disguises were not mutually exclusive

# Version 1.4.2

- You can disable automatic faction updates directly from the "Master of Disguise is ready" message box by clicking "Confirm and Disable Auto Update."

> As in v1.4.1, if you later install mods that change faction relationships, or if faction NPCs are ignoring your disguise, you should re-enable this setting, save, and reload that save to update faction relations again. This is your responsibility.
{.is-warning}

- You can toggle whether guards are hostile to the player while in the Dark Brotherhood disguise using the "Guards vs. Dark Brotherhood Disguise" option.
- You can toggle whether guards are hostile to the player while in the Thieves Guild disguise using the "Guards vs. Thieves Guild Disguise" option.
- The "Guards vs. Dark Brotherhood" toggle menu label and help text were clarified. It is now named "Guards vs. Dark Brotherhood NPCs." The help text now indicates the player will be affected if the player has joined the Dark Brotherhood.
- The "Guards vs. Thieves Guild" toggle menu label and help text were clarified. It is now named "Guards vs. Thieves Guild NPCs."  The help text now indicates the player will be affected if the player has joined the Thieves Guild.
- The Bandit Disguise settings were moved to under the new Banditry heading on the Crime page.
- The "Factions Update Auto Run" menu label on the Advanced page was renamed "Auto Update Factions."
- The currently disabled crime tracker was moved to its own page.

# Version 1.4.1

- A setting has been added to the Advanced menu that allows you to disable automatic faction updates (i.e., Factions Update Auto Run.) After updating once, you can toggle this setting, save, and when loading that save, you will not see the update message box again.

> If you later install mods that change faction relationships, or if faction NPCs are ignoring your disguise, you should re-enable this setting, save, and reload that save to update faction relations again. This is your responsibility.
{.is-warning}

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
<!-- TITLE: Auto Loot -->

If you want to see more free, well-documented mods with detailed patch notes, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

[![https://www.patreon.com/fireundubh](https://i.imgur.com/llPEyru.png)](https://www.patreon.com/fireundubh)

# Version History

## Quick Links

* [Documentation](auto-loot/documentation)
* [Architecture](auto-loot/architecture)
* [Roadmap @ Trello](https://trello.com/b/MTUBalXu/auto-loot-roadmap)
* [Source Code @ GitHub](https://github.com/fireundubh/fallout4/tree/master/Auto%20Loot)
* [Download @ Fallout 4 Nexus](https://www.nexusmods.com/fallout4/mods/27719)

## Version 1.2 - Major Update

This update has not been released.

### New Features

#### Currency Filter

The Currency Filter will loot the following items: Bottlecaps, Pre-War Money, Caps Stashes, Bobby Pins and Bobby Pin Boxes, Bottlecaps via Bottlecap Mines, and Bottlecaps via Fortune Finder IV.

#### Ammo Filter Support for Fusion Cores

The Ammo Filter will loot all Fusion Cores, excluding fusion cores installed in power generators. Auto Loot will not loot fusion cores installed in power generators because removing them via Auto Loot would not trigger the generator shutdown event.

#### Weapons Filter Customization

The Weapons Filter has been upgraded to the newly created tiered filter system. You can configure the Weapons Filter to loot only Big Guns, Energy Weapons, Explosives, Melee Weapons, Small Guns, Traps, Unarmed Weapons. The filter is configured to loot all weapons by default.

#### Valuables Filter Customization

The Valuables Filter has also been upgraded to the tiered filter system. You can configure the Valuables Filter to loot only junk with Common, Uncommon, or Rare components. The filter is configured to loot only junk with Rare components by default. Additionally, you can also configure the Valuables Filter to loot Component Scrap, such as the miscellaneous component items you can pick up and component shipments. This extra option was added primarily for players of certain workshop mods.

#### Dynamic Ash and Goo Pile Prevention

Ash and Goo Piles are activators with hardcoded behaviors; they are neither bodies nor containers. Papyrus offers no support for manipulating these activators and therefore they cannot be supported by Auto Loot. You can manually loot Ash and Goo Piles, or you can use a new feature that prevents Ash and Goo Piles from being created. This new feature dynamically adds the `NoDisintegrate` keyword to NPCs in the loaded area in a radius of 4096 units.

In order to use this feature, enter the following command at the MAIN MENU: 

```
set AutoLoot_Setting_NoDisintegrate to 1
```

You can set up your `Fallout4.ini` so that the command runs at startup:

```
[General]
sStartingConsoleCommand="set AutoLoot_Setting_NoDisintegrate to 1"
```

You can also toggle the global variable directly in the plugin using xEdit.

* **Note 1:** If you execute this command while in a game, this command will do nothing.
* **Note 2:** Toggling the setting off, or uninstalling the mod, will _not_ rollback any keyword additions made by Auto Loot to previously modified NPCs. It is not possible for this to be implemented.

### User Interface

v1.2 streamlines the holotape menu by making the following changes:

* Merged the alphabetized workshop menus into a single menu per filter
* Removed intermediate submenus (e.g., All Filters vs. Specific Filters)
* Removed the Delay Between Iterations submenus from the Debug Menu
* Renamed the Advanced submenu to Advanced Settings
* Renamed the debug-only Advanced submenu to Debug Menu

### Fixed Issues

* Fixed an issue where Automatron armor was not supported by the Armor Filter
* Fixed an issue where an item in a restricted location could be looted, even with Loot Settlements disabled, if the player was outside that location but the item was in the loaded area
* Fixed an issue where dynamic arrays used by Bodies Filter could overpopulate in object-heavy areas
* Fixed an issue where dynamic arrays used by Bodies Filter could overpopulate during optimization

### Optimization / Under the Hood

* Removed unused items from all filter formlists
* Re-sorted all filter formlists by reference count in descending order
* Implemented tiered filter (similar to normal filter but allows filters to be customized with global variables)
* Moderate refactoring, simplified main loops, reduced nesting, and fixed some performance-related logic issues

### Not Yet Implemented

* Added filter-independent toggles for looting while in combat
* Added filter-independent toggles for looting while sneaking
* Added filter-independent toggles for looting legendary armor and weapons

## Version 1.1.4.2 - Hotfix

### Fixed Issue

* Fixed an issue where items in locked containers could be looted without Auto Lockpick enabled (Part III)

### Compatibility

* Added a lockpicking perks formlist to support unlocking containers using mod-added perks (i.e., Locksmith perk checks are no longer hardcoded)

## Version 1.1.4.1 - Hotfix

**Version Note:** Because Nexus has [a longstanding bug](https://github.com/Nexus-Mods/web-issues/issues/601) where you cannot replace a file with a new file if the new file has the same version, the version had to be changed.

### Fixed Issue

* Fixed an issue where the 1.1.4 BA2 archive was packaged incorrectly

## Version 1.1.4 - Minor Update

### Fixed Issues

* Fixed an issue where the last item in a given radius was always looted during the next cycle unless the last item was the only item in which case that item was never looted
* Fixed an issue where items in locked containers could be looted without Auto Lockpick enabled (Part II)
* Fixed an issue where locked containers would not be unlocked with Auto Lockpick enabled if the player had added Locksmith 4 (but not Locksmith 1, 2, or 3) through the console
* Implemented formlist-based quest item exclusions for some filters to handle cases where normally non-quest items are used as quest items (e.g., Coffee Cups, Empty Gwinnett Stout Bottles)
* Armor Filter: Removed Grandpa Savoldi's Hat from formlist due to association with quest Fallen Hero
* Junk Filter: Removed Distress Pulser from formlist due to association with quest The Lost Patrol
* Keys Filter: Removed Clarke's Personal Key from formlist due to association with quest Duty or Dishonor
* Keys Filter: Removed Covenant House Key from formlist due to association with quest Human Error
* Keys Filter: Removed Vault 81 Tech Password from formlist due to association with quest Hole in the Wall
* Valuables Filter: Removed Distress Pulser from formlist due to association with quest The Lost Patrol
* Valuables Filter: Removed Fusion Pulse Charge from formlist due to association with quest The Nuclear Option
* Weapons Filter: Removed Deathclaw Gauntlet from formlist due to association with quest The Devil's Due
* Weapons Filter: Removed Thirst Zapper from formlist due to association with quest The Gauntlet


## Version 1.1.3 - Minor Update

### Fixed Issues

* Fixed an issue where items in locked containers could be looted without Auto Lockpick enabled (Part I)
* Fixed several issues where Auto Steal settings were not ignored with Auto Steal disabled

## Version 1.1.2 - Minor Update

### New Features

* Added a Loot Notifications setting in the Advanced submenu

### Fixed Issues

* Fixed an issue where the Auto Steal setting was not obeyed
* Fixed an issue where toggling the Components, Valuables, or Junk filter did not disable the other mutually exclusive filters
* Fixed an issue where the Valuables filter was not properly mutually exclusive with the Components and Junk filters

### Optimization

* Minor refactoring and micro-optimizations

### Usability

* Set the default radius to 256 units (increased from 128 units) because 128 units is too short for some objects (e.g., bathroom mirrors with sinks)
* Set the default Loot Notifications setting to enabled

## Version 1.1.1 - Minor Update

### Fixed Issues

* Fixed an issue where component states in the Select Components menu could not be toggled

## Version 1.1.0 - Major Update

BEFORE UPDATING, YOU WILL NEED TO TURN OFF ALL FILTERS AND SAVE YOUR GAME. All Form IDs have been changed.

If you skip this step, you will need to reinstall 1.0 to turn off the loot filters. Failing to do either may not release running scripts from memory and those scripts will loop forever, which is bad. Do not skip this step.

### New Features

* Added full support for the Automatron DLC, including items, workshops, and locations
* Added full support for the Far Harbor DLC, including items, workshops, and locations
* Added full support for the Nuka World DLC, including items, workshops, and locations
* Added a Pause/Resume feature that retains filter state settings
* Added an Armor filter for automatically looting clothing, headwear, and facewear
* Added a Components filter for automatically looting junk with specific components
* Added a Keys filter for automatically looting keys
* Added a Magazines filter for automatically looting magazines
* Added a Weapons filter for automatically looting ranged, melee, and throwing weapons
* Added a Take Any filter mode that allows you to, for example, loot only ammo from bodies
* Added filter-independent radius settings
* Added filter-independent destination settings
* Added persistent destination settings

### Fixed Issues

* Fixed an issue where the game would crash for some users when sending loot to the player
* Fixed an issue where Scaleform would crash the game when items were looted while in VATS mode
* Fixed an issue where the Auto Loot Holotape would occasionally not be added to the player
* Fixed an issue where the 128 units radius toggle for some filters would not change states
* Fixed an issue where the player had to reset the destination to the player to disable sending loot to a workshop
* Fixed an issue where bodies were disabled when looted regardless of settings
* Fixed an issue where some actor types were not automatically looted by the Bodies Filter
* Fixed an issue where some Footlockers were not automatically looted by the Containers Filter
* Fixed an issue where some Suitcases were not automatically looted by the Containers Filter
* Fixed an issue where armor was not looted from containers while using the Take Any filter mode
* Fixed an issue where selecting the Radius submenu for the Weapons Filter displayed as a blank terminal
* Fixed a number of issues where None values could theoretically be passed to critical functions
* Fixed an issue where dynamic arrays could overpopulate in object-heavy areas
* Fixed an issue where dynamic arrays could overpopulate during optimization
* Fixed an issue where the Loot Settlements location check could have no return path
* Fixed a number of issues where a boolean function could have no return path

### Optimization

* Significantly improved performance of all filters (e.g., filters now look for most common items first)
* Significantly improved performance of the Take Any filter mode
* Repopulated formlists using playable item tables from Nukapedia
* General housekeeping (e.g., removed unused scripts and terminal script fragments)

### Usability

* Set default radius to 128 units
* Set default destination to the Sanctuary Hills workshop
* Set default destination rule to _send to player_
* Merged similar submenus, such as Base Filters and Special Filters
* Removed filter state toggle from Main menu (deprecated)
* Removed "reset destination to player" from Destination submenu (deprecated)
* Removed "toggle delay before loot" from Advanced submenu (deprecated)
* Renamed submenus to improve clarity (e.g., _Distance_ is now _Radius_, _Containers_ is now _Destinations_)
* Renamed menu items to improve clarity (e.g., _send to player or settlement_ is now _send to workshop_)

### Compatibility

* Pre-War actor no longer used as off-stage storage for Bodies and Containers filters

### Notes

**Destination Rules:** Rules (formerly Exclusions) are used to enable/disable sending loot to a workshop for either all filters or specific filters. Previously, you had to reset the destination to the player to disable sending loot to a workshop. If you decided to send loot to a workshop again, you had to find the workshop in the menu again. Now, your preferred workshop choice will persist, and you only need to flip a switch to toggle whether loot accumulates there.

**Secret Debug Menu:** To enable: `set AutoLoot_Debug to 1`. To disable: `set AutoLoot_Debug to 0`. The debug menu offers these options:

- **Retrieve Lost Items:** In the event that Papyrus blows up and looted items aren't added to your inventory, you can try to recover them from the off-stage dummy actors.
- **Set Delay Between Iterations:** You can set Auto Loot to wait 0-5 seconds between runs, which can, in theory, increase reliability. Possible placebo, mostly a placeholder.
- **Holotapes Filter submenus:** Looting holotapes is not supported by the game, so this filter and its various submenus were hidden. These are placeholders and do nothing.

### Special Thanks

- **Arthmoor**, for creating the dummy actor storage cell and dummy actors
- **computeteen5**, for investigating workarounds to game engine issues
- **SKK**, for advising on fixing the holotape quest script
- **Patreon/PayPal Backers**, for testing pre-release versions

## Version 1.0 - Initial Release

- Initial re-release
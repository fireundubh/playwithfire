<!-- TITLE: Auto Loot -->

If you want to see more mods like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Auto Loot
## Documentation

[Read Documentation](auto-loot/documentation)

## Version History

### Version 1.1.4 - Hotfix (Unreleased)

#### Fixed Issues

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


### Version 1.1.3 - Hotfix

#### Fixed Issues

* Fixed an issue where items in locked containers could be looted without Auto Lockpick enabled (Part I)
* Fixed several issues where Auto Steal settings were not ignored with Auto Steal disabled

### Version 1.1.2 - Hotfix

#### New Features

* Added a Loot Notifications setting in the Advanced submenu

#### Fixed Issues

* Fixed an issue where the Auto Steal setting was not obeyed
* Fixed an issue where toggling the Components, Valuables, or Junk filter did not disable the other mutually exclusive filters
* Fixed an issue where the Valuables filter was not properly mutually exclusive with the Components and Junk filters

#### Optimization

* Minor refactoring and micro-optimizations

#### Usability

* Set the default radius to 256 units (increased from 128 units) because 128 units is too short for some objects (e.g., bathroom mirrors with sinks)
* Set the default Loot Notifications setting to enabled

### Version 1.1.1 - Hotfix

#### Fixed Issues

* Fixed an issue where component states in the Select Components menu could not be toggled


### Version 1.1

BEFORE UPDATING, YOU WILL NEED TO TURN OFF ALL FILTERS AND SAVE YOUR GAME. All Form IDs have been changed.

If you skip this step, you will need to reinstall 1.0 to turn off the loot filters. Failing to do either may not release running scripts from memory and those scripts will loop forever, which is bad. Do not skip this step.

#### New Features

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

#### Fixed Issues

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

#### Optimization

* Significantly improved performance of all filters (e.g., filters now look for most common items first)
* Significantly improved performance of the Take Any filter mode
* Repopulated formlists using playable item tables from Nukapedia
* General housekeeping (e.g., removed unused scripts and terminal script fragments)

#### Usability

* Set default radius to 128 units
* Set default destination to the Sanctuary Hills workshop
* Set default destination rule to _send to player_
* Merged similar submenus, such as Base Filters and Special Filters
* Removed filter state toggle from Main menu (deprecated)
* Removed "reset destination to player" from Destination submenu (deprecated)
* Removed "toggle delay before loot" from Advanced submenu (deprecated)
* Renamed submenus to improve clarity (e.g., _Distance_ is now _Radius_, _Containers_ is now _Destinations_)
* Renamed menu items to improve clarity (e.g., _send to player or settlement_ is now _send to workshop_)

#### Compatibility

* Pre-War actor no longer used as off-stage storage for Bodies and Containers filters

#### Notes

**Destination Rules:** Rules (formerly Exclusions) are used to enable/disable sending loot to a workshop for either all filters or specific filters. Previously, you had to reset the destination to the player to disable sending loot to a workshop. If you decided to send loot to a workshop again, you had to find the workshop in the menu again. Now, your preferred workshop choice will persist, and you only need to flip a switch to toggle whether loot accumulates there.

**Secret Debug Menu:** To enable: `set AutoLoot_Debug to 1`. To disable: `set AutoLoot_Debug to 0`. The debug menu offers these options:

- **Retrieve Lost Items:** In the event that Papyrus blows up and looted items aren't added to your inventory, you can try to recover them from the off-stage dummy actors.
- **Set Delay Between Iterations:** You can set Auto Loot to wait 0-5 seconds between runs, which can, in theory, increase reliability. Possible placebo, mostly a placeholder.
- **Holotapes Filter submenus:** Looting holotapes is not supported by the game, so this filter and its various submenus were hidden. These are placeholders and do nothing.

#### Special Thanks

- **Arthmoor**, for creating the dummy actor storage cell and dummy actors
- **computeteen5**, for investigating workarounds to game engine issues
- **SKK**, for advising on fixing the holotape quest script
- **Patreon/PayPal Backers**, for testing pre-release versions

### Version 1.0

- Initial re-release
<!-- TITLE: Auto Loot -->

If you want to see more mods like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Auto Loot
## Documentation

[Read Documentation](auto-loot/documentation)

## Version History

### Version 1.1

BEFORE UPDATING, YOU WILL NEED TO TURN OFF ALL FILTERS AND SAVE YOUR GAME. All Form IDs have been changed.

If you skip this step, you will need to reinstall 1.0 to turn off the loot filters. Failing to do either may not release running scripts from memory and those scripts will loop forever, which is bad. Do not skip this step.

#### New Features

* Added full support for the Automatron DLC, including items, workshops, and locations
* Added full support for the Far Harbor DLC, including items, workshops, and locations
* Added full support for the Nuka World DLC, including items, workshops, and locations
* Added an Armor filter for automatically looting clothing, headwear, and facewear
* Added a Components filter for automatically looting junk with specific components
* Added a Keys filter for automatically looting keys
* Added a Magazines filter for automatically looting magazines
* Added a Weapons filter for automatically looting ranged, melee, and throwing weapons
* Added a Take Any filter mode that allows you to, for example, loot only ammo from bodies
* Added filter-independent radius settings
* Added filter-independent destination settings
* Added persistent destination settings

#### Fixes

* Fixed an issue where the game would crash for some users when sending loot to the player
* Fixed an issue where Scaleform would crash the game when items were looted while in VATS mode
* Fixed an issue where the Auto Loot Holotape would occasionally not be added to the player
* Fixed an issue where the 128 units radius toggle for some filters would not change states
* Fixed an issue where the player had to reset the destination to the player to disable sending loot to a workshop
* Fixed an issue where some bodies were not automatically looted
* Fixed an issue where some footlockers were not automatically looted
* Fixed an issue where some suitcases were not automatically looted

#### Optimization

* Significantly improved performance of all filters (e.g., filters now look for most common items first)
* Significantly improved performance of the Take Any filter mode
* Repopulated formlists using playable item tables from Nukapedia
* Removed unused scripts

#### Usability

* Set default radius to 128 units
* Set default destination to the Sanctuary Hills workshop
* Reset default destination rule from _send to workshop_ to _send to player_
* Merged similar submenus, such as Base Filters and Special Filters
* Removed deprecated options, such as "reset destination to player" and "toggle delay before loot"
* Renamed submenus to improve clarity (e.g., _Distance_ is now _Radius_, _Containers_ is now _Destinations_)
* Renamed menu items to improve clarity (e.g., _send to player or settlement_ is now _send to workshop_)

#### Compatibility

* Pre-War actor no longer used as off-stage storage for Bodies and Containers filters

#### Notes

**Destination Rules:** Rules (formerly Exclusions) are used to enable/disable sending loot to a workshop for either all filters or specific filters. Previously, you had to reset the destination to the player to disable sending loot to a workshop. If you decided to send loot to a workshop again, you had to find the workshop in the menu again. Now, your preferred workshop choice will persist, and you only need to flip a switch to toggle whether loot accumulates there.

#### Special Thanks

- **Arthmoor**, for creating the dummy actor storage cell and dummy actors
- **computeteen5**, for investigating workarounds to game engine issues
- **SKK**, for advising on fixing the holotape quest script
- **Patreon/PayPal Backers**, for testing pre-release versions

### Version 1.0

- Initial re-release

## To-Do List

- **Components Filter:** Loot items based on what components they offer. Choose from among 32 components. Replaces the Valuables Filter.
- **Keys Filter:** Loot keys. All or nothing.
- **Magazines Filter:** Loot magazines. Choose which magazines.
- **Quest Items Filter:** Loot quest items. Quest items will not be looted via the other filters.
- **Auto Scrap:** Automatically scrap items based on what components they offer - within settlements and/or without.
- **Per-Filter Advanced Settings:** All current and future advanced settings will be toggleable per filter. For example, you could allow stealing but only while crouched, or you could allow harvesting but only while in settlements, or you could allow looting Bodies but only when not in combat.

## Frequently Asked Questions

**I am experiencing crashes. Is Auto Loot at fault?**
Auto Loot v1.0 can exacerbate a game engine issue where adding items to the player using the Activate() method in rapid succession can cause the game to crash. This issue exists with or without Auto Loot installed; however, players are unlikely to encounter the issue through normal play. This issue can be resolved only by Bethesda Softworks. 

**What can I do about crashes?**
As a workaround, the next update will modify all filters so that they add items to off-stage NPCs using the Activate() method, which will in turn transfer their inventories to the player. Until such time that the next update is released, players experiencing stability issues are advised to configure Auto Loot so that items are looted to a workshop. Although this can be inconvenient, the "send to settlement" feature uses the same or similar workaround that will be available to all filters in the next update.

**When is the next update coming out?**
When it's done.
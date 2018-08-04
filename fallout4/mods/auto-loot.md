<!-- TITLE: Auto Loot -->

If you want to see more mods like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Auto Loot
## Version History

### Version 1.0

- Initial re-release

### Version 1.1

Category | Note
--- | ---
Requirements | Auto Loot now requires the Nuka World DLC
New Feature | Added Armor Filter
New Feature | Added Weapons Filter
New Feature | Added support for the Nuka-World Red Rocket settlement
New Feature | Added support for items added by the Automatron, Far Harbor, and Nuka World DLC
New Feature | Added Advanced>Settings toggle for Allow Looting While In Combat
New Feature | Added Advanced>Settings toggle for Allow Looting While Sneaking
New Feature | Added Advanced>Settings toggle for Allow Looting Legendary Items
New Feature | Restored Take Any filter mode to Advanced submenu, allowing filters to be used as "shopping lists"
New Feature | Added DLC settlements to possible Destinations (Note: In 1.0, the menus are there, but the underlying code wasn't implemented.)
Configuration | Changed defaults for all Destination Rules from "send to settlement" to "send to player"
Stability | All filters now use dummy actors to loot and transfer items to (hopefully) avoid a Papyrus crash
Stability | Prevented items from being looted while in VATS mode to avoid a Scaleform crash
Optimization | Sorted formlists by reference count (i.e., filters now look for most common items first)
Optimization | Significantly improved performance of all filters
Optimization | Significantly improved performance of the Take Any filter mode
Optimization | Micro-optimized holotape menus
Compatibility | Pre-War NPC no longer used as temporary storage for Bodies and Containers filters
UI / Holotape | Merged the "Base Filters" and "Special Filters" submenus
UI / Holotape | Renamed Destinations>Exclusions to Destinations>Rules
UI / Holotape | Removed "reset to player" option in the Containers submenu because this is no longer possible
UI / Holotape | Removed "toggle delay before loot" option because this was ultimately pointless
UI / Holotape | Removed unused scrap component filter because implementation was never finished 
UI / Holotape | Renamed "Distance" submenus to "Radius" to improve clarity
UI / Holotape | Renamed "Containers" submenus to "Destinations" to avoid confusion with Containers filter
UI / Holotape | Renamed "send to player or settlement" to "send to settlement"
UI / Holotape | Fixed an issue where the 128 units radius option for Special Filters would not change states correctly
UI / Holotape | Fixed an issue where you had to reset the destination to the player to disable sending loot to a workshop
Upkeep | Repopulated formlists using item tables listed on Nukapedia
Upkeep | Removed unused scripts from package

#### Notes

**Destination Rules:** Rules (formerly Exclusions) are used to enable/disable sending loot to a workshop for either all filters or specific filters. Previously, you had to reset the destination to the player to disable sending loot to a workshop. If you decided to send loot to a workshop again, you had to find the workshop in the menu again. Now, your preferred workshop choice will persist, and you only need to flip a switch to toggle whether loot accumulates there.

#### Special Thanks

- Arthmoor, for creating the dummy actor storage cell and dummy actors
- computeteen5, for investigating workarounds to game engine issues
- SKK, for advising on fixing the holotape quest script
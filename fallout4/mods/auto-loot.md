<!-- TITLE: Master of Disguise -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Master of Disguise
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
UI | Merged the "Base Filters" and "Special Filters" submenus
UI | Renamed Destinations>Exclusions to Destinations>Rules
UI | Removed "reset to player" option in the Containers submenu because this is no longer possible
UI | Removed "toggle delay before loot" option because this was ultimately pointless
UI | Removed unused scrap component filter because implementation was never finished 
UI | Renamed "Distance" submenus to "Radius" to improve clarity
UI | Renamed "Containers" submenus to "Destinations" to avoid confusion with Containers filter
UI | Renamed "send to player or settlement" to "send to settlement"
UI | Fixed an issue where the 128 units radius option for Special Filters would not change states correctly
Upkeep | Repopulated formlists using item tables listed on Nukapedia
Upkeep | Removed unused scripts from package
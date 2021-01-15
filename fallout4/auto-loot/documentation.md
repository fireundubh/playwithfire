---
title: Auto Loot Documentation
description: 
published: true
date: 2021-01-15T17:31:57.736Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:11:25.812Z
---

# Holotape Menu Guide

## Glossary

- **Destination**: A container where items will be stored; can be either the player or a workshop
- **Filter**: A script that loots specific types of items, like a shopping list, strainer/sieve, or gold pan
- **Radius**: Area around the player to be searched, measured in Bethesda Units. 128 units is the height of a normal humanoid actor whereas 4096 is the length of a cell.

## Menu Descriptions

Menu Name | Description
:--- | :---
Main Menu | From the **Main Menu**, you can pause/resume enabled filters. You can also find your way to the Radius, Filters, Destinations, Ownership, Advanced Settings, and Debug Menu submenus.
Radius | From the **Radius** menu, you can set a global radius for All filters, or you can define the radius for each filter.
Filters | From the **Filters** menu, you can enable and disable filters for all supported item types.
Destinations | From the **Rules>Destinations** submenu, you can define the **rules** for all or individual filters. If a filter is set to loot to a workshop, from the **Rules>Filters** submenu, you can select which workshop.
Ownership | From this menu, you can toggle crime-related settings:<br><br>&bull; **Auto Lockpick**: Auto Loot can automatically pick locks, yielding XP and loot from locked containers.<br>&bull; **Auto Steal**: Auto Loot can steal owned loot.<br>&bull; **Auto Steal Reaction**: Auto Loot can steal owned loot without triggering combat.
Advanced | From this menu, you can toggle miscellaneous settings:<br><br>&bull; **Filter Mode**: Can be set to Take All (fast) or Take Any (slow, but precise)<br>&bull; **Loot Notifications**: Can be shown or hidden<br>&bull; **Loot Settlements**: Can be ignored or not; useful for building or tearing down settlements<br>&bull; **Loot Only Actors Killed by Player**: Can loot kills by player or anyone<br>&bull; **Remove Bodies on Loot**: Can disable bodies to declutter the wasteland
Debug | From this menu, you can access debug options:<br><br>&bull; **Retrieve lost items if they exist**: Auto Loot sends items to off-stage dummy actors who then send their items to a destination. This avoids a game bug associated with the player inventory that can cause crashes. If loot appears to be missing, however, there is *a remote, nearly impossible chance* that those items are "backed up" on those off-stage dummy actors. Triggering this option will force them to send their items to the configured destination.


# Pause/Resume

> **Upgrading:** When upgrading to a new version of Auto Loot, pausing is not enough to ensure a clean upgrade. You must *disable all filters* to stop their respective scripts.
{.is-warning}


The Pause/Resume actions can be used to temporarily suspend and continue any enabled filters. This allows you to retain filter states throughout a save.

In addition, these actions are executed more quickly than the previous toggles, which used a loop to add and remove Auto Loot perks.

## Console Commands

You can pause and resume from the console as well.

To pause:

```
set AutoLoot_Setting_PauseLooting to 1
```

To resume:

```
set AutoLoot_Setting_PauseLooting to 0
```

## Hotkeys

You can use a mod like [FO4 Hotkeys](https://www.nexusmods.com/fallout4/mods/11664/) to bind the above console commands to keys.

# Radius

The Radius submenu allows you to set a loot radius for either all filters or specific filters.

Radius | Description
:--- | :---
8192 units | A radius the size of two cells around the player
4096 units | A radius the size of one cell around the player
2048 units | A radius the size of a half-cell around the player
1024 units | A radius the size of a quarter-cell around the player
512 units | A radius the size of four humanoid actors, heightwise, around the player
256 units | A radius the size of two humanoid actors, heightwise, around the player
128 units | A radius the size of a humanoid actor, heightwise, around the player

## Notes

- The radius is effectively planar, meaning that the radius does not extend vertically beyond some engine limit.
- Auto Loot cannot loot objects outside the currently loaded area.

# Filters

The Filters submenu allows you to toggle which filters are enabled. Think of filters as shopping lists.

Filter | Description | Exclusions
:--- | :--- | :---
Ammo | Rounds, shells, cells, harpoons, cannonballs, cells, syringes, and so on | Fusion Cores
Armor | Clothing, headwear, and facewear, excluding power armor for obvious reasons | 
Bodies | Bodies are looted based on whether they are dead, have items, and are associated with an actor type keyword.  |  Some bodies may look like bodies but are actually activators; these are not lootable.
Components | Any junk items you can scrap with specific components |
Containers | Deks, ammo boxes, trash cans, cabinets, toolboxes, etc.  | 
Drinks | Nuka beverages, water, and alcohol  | 
Flora | Anything you can harvest, such as wild carrot flowers and tato plants  | 
Food | Mostly food but includes special consumables such as Stealth Boys | 
Junk | Anything you can scrap | 
Keys | Keys and passwords |
Magazines | Skill magazines | 
Medicine | Stimpaks, Rad-X, and other drugs | 
Valuables | Junk items with rare crafting components | 
Weapons | Guns, big guns, grenades, mines, and close combat weapons | 

**General Exclusions Note:** Activators, such as Caps Stashes and Bobby Pin Boxes, are not lootable by Auto Loot.

## Mutually Exclusive Filters

The Components, Valuables, and Junk filters are all Junk filters and could possibly try to loot the same items regardless of whether they were already looted.

In v1.1, they were made mutually exclusive to avoid performance and/or stability issues. Only one type of Junk filter can be enabled at a time.


# Destinations

The Destinations submenus allow you to send loot to either the player's inventory or a workshop. All settlements are supported.

## Rules

Use the Rules submenu to control where all filters or some filters send loot.

* **Send to player:** Looted items are activated by an off-stage actor who transfers those items to the player. Off-stage actors must act as middlemen to avoid an engine issue.
* **Send to workshop:** Looted items are activated by an off-stage actor who transfers those items to a workshop. The destination workshop defaults to Sanctuary Hills.

**Note:** The All rule is not an override; the All rule is a convenient bulk operation that toggles all rules to either "send to player" or "send to workshop."

# Ownership

The Ownership submenu allows you to control whether Auto Loot obeys locks and item/container ownership.

## Auto Lockpick

* If Auto Lockpick is enabled, locked containers will be picked and reward the appropriate XP before being looted.
* If Auto Lockpick is disabled, locked containers will be ignored by Auto Loot.

## Auto Steal

* If Auto Steal is enabled, Auto Loot will use the Auto Steal settings to determine what to loot.
* If Auto Steal Mode is set to owned and unowned, Auto Loot will loot everything, including items that would otherwise be marked as stolen.
* If Auto Steal Mode is set to only owned, Auto Loot will loot only items that would otherwise be marked as stolen.
* If Auto Steal Reaction is set to hostile, when Auto Loot loots items that would otherwise be marked as stolen, actors will react to the theft.
* If Auto Steal Reaction is set to none, when Auto Loot loots items that would otherwise be marked as stolen, actors will not react to the theft.

# Advanced

The Advanced submenu allows you to toggle some experimental features.

## Filter Mode

* If Filter Mode is set to Take All, when the Bodies and Containers filters are enabled, these filters will take everything. This is the default mode.
* If Filter Mode is set to Take Any, when the Bodies and Containers filters are enabled, these filters will take only specific categories of items. To customize which categories of items are used as shopping lists for the Bodies and Containers filters, enable other filters.

For example, if you want to loot only ammo from bodies, you would set the Filter Mode to Take Any, enable the Bodies filter, and enable the Ammo filter.

## Loot Settlements

* If Loot Settlements is enabled, Auto Loot will loot items, bodies, and containers in settlement regions. The Workshop container is always excluded.
* If Loot Settlements is disabled, Auto Loot will ignore items, bodies, and containers in settlement regions. Disable this option when you don't want your settlement decorations to be looted.

## Remove Bodies On Loot

This is an experimental feature. If you are running the game with Papyrus logging, you will see a lot of harmless warnings.

* If Remove Bodies On Loot is enabled, the Bodies filter will disable bodies when they are looted. Only bodies that have no items will be disabled.
* If Remove Bodies On Loot is disabled, the Bodies filter will not disable bodies when they are looted.

## Delay

**v1.1 Note:** The Delay submenu is no longer available through the holotape.

**v1.2 Note:** The Delay submenu has been deleted, but the global variables can still be changed via the console.

The Delay submenu allows you to slow down the rate at which Auto Loot iterates through shopping lists. The delay can be set to 0, 1, 2, 4, or 5 seconds. If the delay is 0 seconds, which is the default setting, Auto Loot will work as fast as possible.
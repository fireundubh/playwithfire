---
title: Frequently Asked Questions
description: 
published: true
date: 2024-05-20T22:02:57.321Z
tags: 
editor: markdown
dateCreated: 2021-03-19T21:45:25.745Z
---

# Getting Started

## How do I run Auto Loot?

This quick tutorial outlines the steps to getting up-and-running with a basic configuration:

1. Press `Tab` to open the Pip-Boy menu.
2. Go to `Inv > Misc`.
3. Click `> Auto Loot Holotape` to load the holotape.
4. Click `> Radius`.
5. Click `> All`.
6. Choose a radius (recommended: `256`, `512`, `1024`)
7. Press `Tab` repeatedly until you reach the Main Menu.
8. Click `> Filters`.
9. Click `Flora Filter (disabled)` to toggle this filter on. The text will change to `Flora Filter (enabled)`.
10. Press `Tab` repeatedly until you exit the holotape.

Auto Loot will begin looting flora as soon as you exit the holotape.

## Why can't I loot bodies or containers when I turn on other filters?

1. To loot from bodies and/or containers, the Bodies and/or Containers filters must be enabled, respectively.
2. To loot ammo - for example - from bodies and/or containers, the Ammo filter must also be enabled and the [Filter Mode](https://wiki.fireundubh.com/mods/auto-loot/documentation#filter-mode) set to Take Any.

Unless the Bodies and/or Containers filters are enabled, all other filters process only loot *in the world* - as opposed to loot *in bodies and containers*.

## Why can't I loot ash and goo piles?

Ash and Goo Piles are activators with hardcoded behaviors; they are neither bodies nor containers. Papyrus offers no support for manipulating these activators and therefore they cannot be supported by Auto Loot.

You can manually loot Ash and Goo Piles, or you can use a feature that prevents Ash and Goo Piles from being created. This feature dynamically adds the `NoDisintegrate` keyword to NPCs in the loaded area in a radius of 4096 units.

In order to use this feature, enter the following command at the MAIN MENU \[of the game!]: 

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

## Is the Non-Playable Flags Patch necessary?

**YES.** The included plugin `Non-Playable Flags Patch.esp` fixes issues in the vanilla game where NPC skins are not flagged as Non-Playable. The Papyrus function `RemoveAllItems` can remove skins not flagged correctly and **crash the game**, according to some players. Like many vanilla scripts and many other mods, Auto Loot makes use of this function. These issues were reported to the Unofficial Fallout 4 Patch Project and the project maintainer Arthmoor said at the time these issues would be resolved in a future update. Until that happens, I highly recommend keeping this plugin enabled.

# Filters

## What is a filter?

A filter is, fundamentally, an instance of a script that:

* uses a formlist to find all references to items in the loaded area;
* iterates through the resulting `ObjectReference` array; and
* executes loot actions on each array item that matches specific conditions.

## What is filter customization?

Filter customization exposes key decision points in a filter script to the user through global variables. By changing these variables, users can control the flow of the script's execution.

## How do I add support for other mods?

By default, Auto Loot supports only items in the base game, Automatron, Far Harbor, and Nuka World. Support for items unique to other mods can be added to the relevant filter formlists. These formlists are merely categorized collections of forms, sorted by reference count in descending order.

Filter | Type | Script | Notes 
:--- | :--- | :--- | :---
Ammo | Shared | `dubhAutoLootEffectScript` |
Armor | Shared | `dubhAutoLootEffectScript` |
Bodies | Keywords | `dubhAutoLootEffectBodiesScript` | Unique functionality for building an `ObjectReference` array from actor type keywords, handling actors, and using other filters to loot specific categories of items
Components | Components | `dubhAutoLootEffectComponentsScript` | Unique functionality for testing whether items have specific components
Containers | Containers | `dubhAutoLootEffectContainersScript` | Unique functionality for handling containers and using other filters to loot specific categories of items
Currency | Shared | `dubhAutoLootEffectScript` |
Drinks | Shared | `dubhAutoLootEffectScript` |
Flora | Shared | `dubhAutoLootEffectScript` |
Food | Shared | `dubhAutoLootEffectScript` |
Holotapes | Shared | `dubhAutoLootEffectScript` |
Junk | Shared | `dubhAutoLootEffectScript` |
Keys | Shared | `dubhAutoLootEffectScript` |
Magazines | Shared | `dubhAutoLootEffectScript` |
Medicine | Shared | `dubhAutoLootEffectScript` |
Valuables | Tiered | `dubhAutoLootEffectTieredScript` | Unique functionality for handling multi-dimensional formlists with a depth of 2
Weapons | Tiered | `dubhAutoLootEffectTieredScript` | Unique functionality for handling multi-dimensional formlists with a depth of 2

### Tiered Filters

Tiered filters include the Valuables and Weapons Filters. A tiered filter has a parent formlist that contains child formlists. For example:

```text
AutoLoot_Filter_Valuables
  > AutoLoot_Filter_Valuables_Common
  > AutoLoot_Filter_Valuables_Uncommon
  > AutoLoot_Filter_Valuables_Rare
  > AutoLoot_Filter_Valuables_Components
```

Each child formlist is a standard collection of items as used by Shared filters, paired with a global variable that the script uses to determine whether the child formlist should be used to build and process references.


# Logging

## How do I enable Papyrus logging?

In `Fallout4.ini`, add or change this section to match the following block:

```
[Papyrus]
fPostLoadUpdateTimeMS=500.0
bEnableLogging=1
bEnableTrace=1
bLoadDebugInformation=1
```

Papyrus logging must be enabled at the INI level for log messages to be saved to disk.

- If logging is not enabled at the INI level, you will not be able to view or share your logs.
- If logging is disabled in the MCM menu, the mod will not produce any log messages.

I recommend disabling Papyrus logging at the INI level after retrieving the necessary information.

The Papyrus logger CANNOT help you solve crashes. When the game crashes, the logger crashes, too.

Most experienced mod authors recommend that you disable logging when it is not needed because the logger can be detrimental to the stability and performance of the game. In fact, SmkViper — the creator of Papyrus at Bethesda Softworks — added a similar warning to the top of all Papyrus logs produced by Fallout 4.

Enable the Papyrus logger only when you need to debug scripts or produce logs that can help mod authors investigate issues.


## Where can I find the logs?

The latest Papyrus log is saved to this file:

```
%USERPROFILE%\Documents\My Games\Fallout4\Logs\Script\Papyrus.0.log
```

Logs specific to Auto Loot are saved in this folder:

```
%USERPROFILE%\Documents\My Games\Fallout4\Logs\Script\User
```


## Where can I post my Papyrus log?

Use [Hastebin](https://hastebin.com/), [Pastebin](https://pastebin.com/), or [GitHub Gists](https://gist.github.com/) to post your log.

You can upload your log in the `#autoloot` channel on [my Discord server](https://discord.fireundubh.com). Please do not post only the log. To the best of your ability, explain the issue and articulate the behavior you expected.

The log alone will not help me investigate and resolve your issue.
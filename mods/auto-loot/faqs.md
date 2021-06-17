---
title: Frequently Asked Questions
description: 
published: true
date: 2021-06-17T08:18:25.829Z
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


# Filters

## What is a filter?

A filter is, fundamentally, an instance of a script that:

* uses a formlist to find all references to items in the loaded area;
* iterates through the resulting `ObjectReference` array; and
* executes loot actions on each array item that matches specific conditions.

## What is filter customization?

Filter customization exposes key decision points in a filter script to the user through global variables. By changing these variables, users can control the flow of the script's execution.

## How do I create a new filter?

This chart shows new records in yellow, their immediate ancestors, and their descendants. Connections can be either properties, conditions, or elements, such as formlist items.

**Note:** Chart removed temporarily until I create a new version.

There is much, much more to creating a new filter than shown in the chart. For example, each terminal has a sequence of menu items, each global variable has a default value, and every other record has a number of properties mostly related to filter customization settings. In addition, almost every terminal has a script fragment, which is generated automatically by an xEdit script framework engineered specifically for Auto Loot. In fact, there are 20-30 xEdit scripts that are regularly used to update Auto Loot and add new features.

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
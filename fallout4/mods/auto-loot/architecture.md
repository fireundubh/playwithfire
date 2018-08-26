<!-- TITLE: Architecture -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# How Auto Loot Works
This is a working document.

## Filters

### What is a filter?

A filter is, fundamentally, an instance of a script that:

* uses a formlist to find all references to items in the loaded area;
* iterates through the resulting `ObjectReference` array;
* pares down that array using specific conditions and produces a new `ObjectReference` array;
* iterates through the stripped down `ObjectReference` array; and
* executes a loot action on each item in that array.

### What is filter customization?

Filter customization exposes key decision points in a filter script to the user through global variables. By changing these variables, users can control the flow of the script's execution.

### How do I create a new filter?

This chart shows new records in yellow, their immediate ancestors, and their descendants. Connections can be either properties, conditions, or elements, such as formlist items.

![How to Create a New Filter](https://i.imgur.com/G6XGGPA.png)

There is much, much more to creating a new filter than shown in the chart. For example, each terminal has a sequence of menu items, each global variable has a default value, and every other record has a number of properties mostly related to filter customization settings. In addition, almost every terminal has a script fragment, which is generated automatically by an xEdit script framework engineered specifically for Auto Loot. In fact, there are 20-30 xEdit scripts that are regularly used to update Auto Loot and add new features.

### How do I add support for other mods?

By default, Auto Loot supports only items in the base game, Automatron, Far Harbor, and Nuka World. Support for items unique to other mods can be added to the relevant filter formlists. These formlists are merely categorized collections of forms, sorted by reference count in descending order.

Filter | Type | Script | Notes 
:--- | :--- | :--- | :---
Ammo | Shared | `dubhAutoLootEffectScript` |
Armor | Shared | `dubhAutoLootEffectScript` |
Bodies | Keywords | `dubhAutoLootEffectBodiesScript` | Unique functionality for building an `ObjectReference` array from actor type keywords, handling actors, and using other filters to loot specific categories of items
Components | Shared (Modified) | `dubhAutoLootEffectComponentsScript` | Unique functionality for testing whether items have specific components
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

#### Tiered Filters

Tiered filters include the Valuables and Weapons Filters. A tiered filter has a parent formlist that contains child formlists. For example:


```text
AutoLoot_Filter_Valuables
  > AutoLoot_Filter_Valuables_Common
  > AutoLoot_Filter_Valuables_Uncommon
  > AutoLoot_Filter_Valuables_Rare
  > AutoLoot_Filter_Valuables_Components
```

Each child formlist is a standard collection of items as used by Shared filters, paired with a global variable that the script uses to determine whether the child formlist should be used to build and process references.
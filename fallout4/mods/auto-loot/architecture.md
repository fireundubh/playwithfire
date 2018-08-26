<!-- TITLE: Architecture -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# How Auto Loot Works
This is a working document.

## Filters

### What is a filter?

A filter is, fundamentally, an instance of a script that:

* uses a formlist to find all references to items in the loaded area;
* iterates through the resulting ObjectReference array;
* pares down that array using specific conditions and produces a new ObjectReference array;
* iterates through the stripped down ObjectReference array; and
* executes a loot action on each item in that array.

### What is filter customization?

Filter customization exposes key decision points in a filter script to the user through global variables. By changing these variables, users can control the flow of the script's execution.

### Creating a new filter

This chart shows new records in yellow, their immediate ancestors, and their descendants. Connections can be either properties, conditions, or elements, such as formlist items.

![How to Create a New Filter](https://i.imgur.com/G6XGGPA.png)

There is much, much more to creating a new filter than shown in the chart. For example, each terminal has a sequence of menu items, each global variable has a default value, and every other record has a number of properties mostly related to filter customization settings. In addition, almost every terminal has a script fragment, which is generated automatically by an xEdit script framework engineered specifically for Auto Loot. In fact, there are 20-30 xEdit scripts that are regularly used to update Auto Loot and add new features.

<!-- TITLE: Architecture -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# How Auto Loot Works
This is a working document

## Filters

### What is a filter?

A filter is, fundamentally, an instance of a script that:

* uses a formlist to find all references to items in the loaded area;
* iterates through the resulting ObjectReference array;
* pares down that array using specific conditions and produces a new ObjectReference array;
* iterates through the stripped down ObjectReference array; and
* executes a loot action on each item in that array.

### Creating a new filter

This chart shows new records in yellow, their immediate ancestors, and their descendants. Connections can be either properties, conditions, or elements, such as formlist items.

![How to Create a New Filter](https://i.imgur.com/G6XGGPA.png)


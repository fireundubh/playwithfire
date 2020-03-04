---
title: Frequently Asked Questions
description: 
published: true
date: 2020-03-04T07:15:24.366Z
tags: 
---

# Logging

## How do I enable Papyrus logging?

In `Skyrim.ini`, add or change this section match the following block:

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

The Papyrus logger CANNOT help you solve crashes. When the game crashes, the logger crashes, too. The Papyrus log is not a crash dump and the game does not produce crash dumps.

Also, the logger may be detrimental to the stability and performance of the game. Enable the Papyrus logger only when you need to debug scripts or produce logs that can help mod authors investigate issues.


## Where can I find the logs?

Papyrus logs are stored at:

```
%USERPROFILE%\Documents\My Games\Skyrim Special Edition\Logs\Script\Papyrus.0.log
```


## Where can I post my Papyrus log?

Use [Hastebin](https://hastebin.com/), [Pastebin](https://pastebin.com/), or [GitHub Gists](https://gist.github.com/) to post your log.

You can upload your log in the `#masterofdisguise` channel on [my Discord server](https://discord.fireundubh.com). Please do not post only the log. To the best of your ability, explain the issue and articulate the behavior you expected.

The log alone will not help me investigate and resolve your issue.


# Extending Disguises

## Components

For each disguise in the SSE version of Master of Disguise, there is:

- 1 disguise formlist
- 1 disguise slots formlist, and
- 8 formlists for each disguise slot.

Every formlist is used, so if you are adding items, you need to add items to every formlist as appropriate.

> **Note:** In the Classic or Legendary version of Master of Disguise, each disguise is comprised of only a single formlist.


### Example

FormList | Description
:--- | :---
`dubhDisguiseVampires` | Contains all items in the slot formlists
`dubhDisguiseVampires_Slots` | Contains all slot formlists
`dubhDisguiseVampires_Slot_0_Hair` | Contains only items that are equipped in the Hair slot
`dubhDisguiseVampires_Slot_1_Body` | Contains only items that are equipped in the Body slot
`dubhDisguiseVampires_Slot_2_Hands` | Contains only items that are equipped in the Hands slot
`dubhDisguiseVampires_Slot_3_Amulet` | Contains only items that are equipped in the Amulet slot
`dubhDisguiseVampires_Slot_4_Ring` | Contains only items that are equipped in the Ring slot
`dubhDisguiseVampires_Slot_5_Feet` | Contains only items that are equipped in the Feet slot
`dubhDisguiseVampires_Slot_6_Shield` | Contains only items that are equipped in the Shield slot
`dubhDisguiseVampires_Slot_7_Circlet` | Contains only items that are equipped in the Circlet slot


## Slots

Each slot formlist corresponds to the Biped Body Template First Person Flags on ARMO records. For example, the Vampire Hood has the Hair and Circlet flags, which means the item equips in the Hair and Circlet slots. Consequently, the Vampire Hood is a member of both `0_Hair` and `7_Circlet` formlists.

![xEdit Screenshot](https://i.imgur.com/aNJaKBr.jpg)

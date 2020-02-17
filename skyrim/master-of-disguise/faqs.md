---
title: Frequently Asked Questions
description: 
published: true
date: 2020-02-17T00:59:12.460Z
tags: 
---

# Where can I find the logs?

You have to enable Papyrus logging in `Skyrim.ini` before you enable disguise/faction/detection system logging.

```
[Papyrus]
fPostLoadUpdateTimeMS=500.0
bEnableLogging=1
bEnableTrace=1
bLoadDebugInformation=1
```

Papyrus logs are stored at:

`%USERPROFILE%\Documents\My Games\Skyrim Special Edition\Logs\Script\Papyrus.0.log`

Disable Papyrus logging after retrieving the necessary information. The Papyrus logger CANNOT help you solve crashes, which are not caused by scripts, and may, in fact, cause instability and other performance issues. Only enable the Papyrus logger when you need to debug scripts.


# Where can I post my Papyrus log?

Use [Hastebin](https://hastebin.com/), [Pastebin](https://pastebin.com/), or [GitHub Gists](https://gist.github.com/) to post your log.

Do NOT post your log in the comments or your post will be deleted.


# How do formlists work? I want to add items to disguises.

## Components

For each disguise in the SSE version of Master of Disguise, there is:

- 1 disguise formlist
- 1 disguise slots formlist, and
- 8 formlists for each disguise slot.

Every formlist is used, so if you are adding items, you need to add items to every formlist as appropriate.

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

## Classic Notes

In the Classic or Legendary version of Master of Disguise, each disguise is comprised of only a single formlist.
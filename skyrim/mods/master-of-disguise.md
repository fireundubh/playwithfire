---
title: Master of Disguise
description: 
published: true
date: 2020-02-17T00:46:10.771Z
tags: 
---

# Useful Console Commands

Command | Default Value | Description
--- | --- | ---
`set iDubhScriptDebugDisguise to [0, 1]` | `0` | Toggles disguise system logging
`set iDubhScriptDebugEnemy to [0, 1]` | `0` | Toggles faction enemy system logging
`set iDubhScriptDebugMonitor to [0, 1]` | `0` | Toggles detection system logging
`set iDubhAlwaysSucceedDremora to [0, 1]` | `1` | Toggles whether Daedric disguises always succeed vs. Dremora
`set iDubhAlwaysSucceedWerewolves to [0, 1]` | `1` | Toggles whether the Savior's Hide always succeeds vs. Werewolves
`AddFormToFormlist xxFF0320 xx027AA9` | | Disables bandit disguises (xx is the load order of Master of Disguise in hex)

# Frequently Asked Questions

## Where can I find the logs?

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


## Where can I post my Papyrus log?

Use [Hastebin](https://hastebin.com/), [Pastebin](https://pastebin.com/), or [GitHub Gists](https://gist.github.com/) to post your log.

Do NOT post your log in the comments or your post will be deleted.


## How do formlists work? I want to add items to disguises.

The non-SKSE version of Master of Disguise uses 1 disguise formlist, 1 disguise slots formlist, and 8 formlists for each disguise slot. For example:

Form List | Description
--- | ---
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

You can check which slots in which an item equips by looking at the item's Biped Body Template first-person flags. For example, the Vampire Hood equips in the Hair and Circlet slots, so the Vampire Hood appears in the respective formlists.

In the SKSE version for classic Skyrim, there's only a single formlist for each disguise, which doesn't really require any explanation.
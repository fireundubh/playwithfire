---
title: Frequently Asked Questions
description: 
published: true
date: 2020-12-26T05:08:56.089Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:11:18.083Z
---

# Logging

## How do I enable Papyrus logging?

In `Skyrim.ini`, add or change this section to match the following block:

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
%USERPROFILE%\Documents\My Games\Skyrim Special Edition\Logs\Script\Papyrus.0.log
```

Logs specific to Master of Disguise are saved in this folder:

```
%USERPROFILE%\Documents\My Games\Skyrim Special Edition\Logs\Script\User\
```


## Where can I post my Papyrus log?

Use [Hastebin](https://hastebin.com/), [Pastebin](https://pastebin.com/), or [GitHub Gists](https://gist.github.com/) to post your log.

You can upload your log in the `#masterofdisguise` channel on [my Discord server](https://discord.fireundubh.com). Please do not post only the log. To the best of your ability, explain the issue and articulate the behavior you expected.

The log alone will not help me investigate and resolve your issue.


# Extending Disguises

## Rules

- There is a single formlist for every disguise.
- Each formlist contains all possible items that comprise each disguise.
- Every item must have the appropriate Biped Body Template First Person Flags.
- Only items in the following slots are evaluated: Hair, Body, Hands, Amulet, Ring, Feet, Shield, and Circlet.
- Disguises with the same essential slot should never share the same item in that slot.


## Slots

### Essential Slots

Index | Slot | Name | Disguise
:--- | :--- | :--- | :---
0 | 31 | Hair | 
1 | 32 | Body | All Disguises Except...
2 | 33 | Hands | 
3 | 35 | Amulet | Vigil of Stendarr
4 | 36 | Ring | Silver Hand
5 | 37 | Feet | 
6 | 39 | Shield | Windhelm Guard
7 | 42 | Circlet | Cultists


### Special Disguises

Disguise | Slot Requirement
:--- | :---
Daedric Influence | Any Slot
Bandit Disguise | Configurable

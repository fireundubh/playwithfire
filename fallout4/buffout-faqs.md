---
title: Buffout 4 FAQs
description: 
published: true
date: 2020-10-03T05:50:57.305Z
tags: 
editor: markdown
---

# Questions

## Where do I find the crash logs?

In the `%USERPROFILE%\Documents\My Games\Fallout4\F4SE` folder, you should find `.log` files with the prefix `crash`. Those are the crash logs.

## The game crashed, but I don't have any crash logs.

If the game crashed and no crash log was generated, Buffout could not capture the exception - for a variety of reasons. There are two relatively easy things you can try:

1. Check the System log in the Windows Event Viewer for Error and Critical events whose timestamps coincide with the time that the game crashed. If you have such events, these events may provide clues for further investigation.
2. For more technical users, you can install [DebugDiag](https://www.microsoft.com/en-us/download/details.aspx?id=58210) from Microsoft, create a crash rule for the `Fallout4.exe` process that logs the stack trace, activate the crash rule, and run the game until you crash. This will produce a detailed log that can be analyzed in DebugDiag and shared.

## How do I read crash logs?

You need a background in programming, debugging, and reverse engineering (RE). Specifically, you need to know assembly, C types, and be familiar with the stack concept. You must also have the tools and skills to load the executable; identify the involved subroutines, logic, and parameters; and statically analyze the stack trace to make your best guess at the error.

There are no easy answers and therefore no easy explanations. There are many gotchas and exceptional cases that require hands-on investigation to rule out. Buffout's crash logs are not intended for most users; they are specifically for Ryan and anyone else in the RE community. 

## Should I post my crash log? My game is heavily modded.

Yes. Always post your *entire* crash log. Please use spoiler tags or Pastebin.

# Common Issues

## flexRelease_x64.dll crashes

Fallout 4 implements a defunct version of [NVIDIA FleX](https://developer.nvidia.com/flex) for weapon debris and other particle effects.

Disable FleX entirely by adding the following lines to `fallout4custom.ini`:

```ini
[NVFlex]
bNVFlexEnable=0
bNVFlexInstanceDebris=0
bNVFlexDrawDebris=0
```

**Note:** In some cases, crashes not logged by Buffout can be traced to not having FleX disabled.

## nvwgf2umx.dll crashes

The `nvwgf2umx.dll` assembly belongs to the NVIDIA driver package. Most likely, you recently updated your video drivers. The `445` drivers appear to be the source of crashes in many games.

Downgrade to the `441` series. You can find links to many older NVIDIA drivers [here](https://github.com/keylase/nvidia-patch/tree/master/win).

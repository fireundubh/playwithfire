---
title: Multiple Game Support
description: 
published: true
date: 2021-05-30T23:07:38.452Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:07:38.452Z
---

Pyro supports each version of the Papyrus Compiler for _Skyrim Classic_ (TES5), _Skyrim Special Edition_ (SSE), and _Fallout 4_ (FO4).

There are multiple ways to change the compiler version:

1. Use the `-g, --game-type` argument to specify one of these games: `fo4`, `sse`, or `tes5`.
2. Use the `--game-path` argument to specify the path to where one of the above games is installed.
3. Use the `--registry-path` argument to specify the path to the `Installed Path` key in the Windows Registry for the respective game.
4. Add the `Game` attribute to the `<PapyrusProject>` element in your Papyrus Project file with one of these values: `fo4`, `sse`, or `tes5`.


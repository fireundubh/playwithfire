---
title: Incremental Build
description: 
published: true
date: 2021-05-30T23:08:56.909Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:08:56.909Z
---

Incremental build _vastly_ accelerates builds by compiling only scripts that *need* to be compiled. Pyro determines which PSC files to compile by comparing the last modified timestamp on PSC files with the compilation timestamps embedded in PEX files. Pyro then spawns multiple workers (compiler instances) in parallel to further reduce build times.

Each instance of the compiler will be executed with "below normal" priority, allowing you to continue working without the Papyrus Compiler significantly impacting the performance of your system.

---
title: Anonymization
description: 
published: true
date: 2021-05-30T23:09:23.747Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:09:23.747Z
---

When the Papyrus Compiler compiles a script, your system username, your computer name's on your local network, and the full path to the source script are embedded in the header. This data can be retrieved using a hex editor or a Papyrus decompiler, such as Champollion. This data could put at risk your security or privacy. Pyro replaces those strings in compiled scripts with random letters.

Simply add the `Anonymize` attribute to the `PapyrusProject` node and set the value to `True`.


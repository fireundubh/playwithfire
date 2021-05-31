---
title: Anonymization
description: 
published: true
date: 2021-05-31T10:25:35.240Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:09:23.747Z
---

When the Papyrus Compiler compiles a script, the following metadata is embedded in that script:

- your system username,
- your computer name's on your local network, and
- the full path to the source script.

This metadata helps game developers find team members responsible for specific scripts during development, but outside team environments, this metadata serves no purpose.

This metadata can be retrieved using a hex editor or a Papyrus decompiler, such as Champollion. This metadata could put at risk your security or privacy.

Pyro anonymizes script metadata by scrambling each string with random letters.

Anonymization can be enabled by adding the `Anonymize` attribute to the `PapyrusProject` node and setting the value to `True`.

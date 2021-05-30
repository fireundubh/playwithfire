---
title: Extended Schema
description: 
published: true
date: 2021-05-30T23:08:27.600Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:08:08.995Z
---

> Refer to the [Pyro Project Schema](/pyro/schema) page for default attribute values.
{.is-info}

> Refer to the [Pyro Project XML Schema Definition](https://github.com/fireundubh/pyro/blob/master/pyro/PapyrusProject.xsd) for document structure, type constraints, and other rules.
{.is-info}


Bethesda Game Studios introduced the PPJ schema with the Papyrus Compiler for FO4. The TES5 and SSE compilers do not support the schema.

Pyro supports all standard PPJ elements and attributes used by the Papyrus Compiler. The PPJ schema has also been extended to support features unique to Pyro.

**Note:** The `Asm` attribute of the `PapyrusProject` node is ignored by Pyro. The Papyrus Compiler uses this attribute to call the Papyrus Assembler but generating assembly files for Papyrus scripts is out-of-scope for Pyro.

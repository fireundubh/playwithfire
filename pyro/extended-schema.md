---
title: Extended Schema
description: 
published: true
date: 2021-06-14T22:45:45.122Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:08:08.995Z
---

Bethesda Game Studios introduced the PPJ schema with the Papyrus Compiler for FO4. The TES5 and SSE compilers do not support Papyrus Projects.

Pyro, however, brings Papyrus Projects to TES5 and SSE, and supports the entire official schema in addition to a ton of new features unique to Pyro.

**Note:** The `Asm` attribute of the `PapyrusProject` node is ignored by Pyro. The Papyrus Compiler uses this attribute to call the Papyrus Assembler but generating assembly files for Papyrus scripts is out-of-scope for Pyro.

## Schema Reference

See: [Pyro Project Schema](/pyro/schema)

## Technical Schema Reference

For information about document structure, type constrains, and other rules, refer to the XSD directly.

See: [Pyro Project XML Schema Definition](https://github.com/fireundubh/pyro/blob/master/pyro/PapyrusProject.xsd)
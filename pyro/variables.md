---
title: Variables
description: 
published: true
date: 2021-05-30T23:18:47.107Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:18:47.107Z
---

Pyro can substitute variables with defined values in PPJ paths and string attributes.

To configure variables:

1. Add a `Variables` node block.
2. Add as many `Variable` nodes to that block as needed.

For example:

```xml
<Variables>
  <Variable Name="namespace" Value="Master of Disguise"/>
  <Variable Name="modname" Value="Master of Disguise - Special Edition"/>
  <Variable Name="myproject" Value="E:\projects\skyrim\Master of Disguise - Special Edition"/>
</Variables>
```

Variables are prefixed with the `@` symbol. The `Name` and `Value` attributes are required.

You can then replace values throughout the project file with variable names:

```xml
<ZipFiles Output="@myproject">
  <ZipFile Name="@modname" RootDir="@myproject" Compression="deflate">
    <Include>@myproject\@modname.esp</Include>
    <Include NoRecurse="true">*.bsa</Include>
  </ZipFile>
<ZipFiles>
```

Pyro will expand those variables when the project is loaded.

In addition, regardless of whether a `Variables` node group is defined, environment variables (e.g., `%APPDATA%`) and user variables (`~user`) will also be expanded.

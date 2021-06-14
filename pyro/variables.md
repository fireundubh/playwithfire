---
title: Variables
description: 
published: true
date: 2021-06-14T12:25:33.619Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:18:47.107Z
---

Pyro can substitute variables with defined values in PPJ paths and string attributes.


# Defining variables

To define variables:

1. Add a `Variables` block.
2. Add as many `Variable` child nodes to that block as needed.


## Example

```xml
<Variables>
  <Variable Name="namespace" Value="Master of Disguise"/>
  <Variable Name="modname" Value="Master of Disguise - Special Edition"/>
  <Variable Name="myproject" Value="E:\projects\skyrim\Master of Disguise - Special Edition"/>
</Variables>
```


# Variable substitution

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


# Environment and user variables

Regardless of whether a `Variables` block is defined, environment variables (e.g., `%APPDATA%`) and user variables (`~user`) will be expanded.

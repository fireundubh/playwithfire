---
title: Packaging
description: 
published: true
date: 2021-06-14T12:19:43.268Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:10:18.847Z
---

Pyro can store scripts and other files in BSA and BA2 packages using [BSArch](https://www.nexusmods.com/newvegas/mods/64745), of which the latest unmodified version is distributed with Pyro under the MPL 2.0 license.


# Defining packages

To configure packages:

1. Add the `Package` attribute to the `PapyrusProject` node. Set the value to `True`.
2. Add a `Packages` block with as many `Package` child blocks as needed.
3. Each `Package` child block can contain as many `Include` and `Match` nodes as needed.


## Example

```xml
<Packages Output="@OutputPath">
  <Package Name="@ModName" RootDir="@OutputPath">
    <Match In="Scripts">*.pex</Match>
    <Match In="Strings">*.*strings</Match>
    <Match In="interface\translations">*.txt</Match>
  </Package>
  <Package Name="@ModName - Textures" RootDir="@OutputPath">
    <Include>*.dds</Include>
  </Package>
</Packages>
```


# Including files

Files can be included in packages using both `Include` and `Match` nodes.

- The `Include` node supports relative file and folder paths, absolute file and folder paths, and glob expressions.
- The `Match` node supports wildcard file patterns, including file negation and directory exclusion patterns.

All matches are case insensitive. Files cannot be matched outside the project root.


## Using the Include node

```xml
<!-- Search for pattern "README.md" from the project path, recursively if not found in the project root -->
<Include NoRecurse="false">README.md</Include>

<!-- Like above but adds the file to the "docs" folder -->
<Include Path="docs">README.md</Include>

<!-- Search for pattern "docs\README.md" from the project path, recursively if not found from the project root -->
<Include>docs\README.md</Include>

<!-- Search for pattern "docs\*.md" from the project path, recursively -->
<Include>docs\*.md</Include>

<!-- Search for all files in the "docs" folder from the project path, recursively -->
<Include>docs</Include>
```


## Using the Match node

```xml
<!-- Match "*.esp" from the project path, recursively -->
<Match>*.esp</Match>

<!-- Match "*.esp" from the project path, recursively, but exclude file matches starting with "optional" -->
<Match>*.esp|-optional</Match>

<!-- Match "*.esp" in only the project path -->
<Match NoRecurse="true">*.esp</Match>

<!-- Match "*.esp" from the "optional" folder in the project path, recursively -->
<Match In="optional">*.esp</Match>

<!-- Match "*.esp" from the "optional" folder in the project path, recursively -->
<Match Exclude="*|-optional">*.esp</Match>

<!-- Match "*.esp" from the project path, recursively, but exclude matches in the "optional" folder -->
<Match Exclude="optional">*.esp</Match>
```


# Temporary files

The packaging system uses a default temporary folder, or a folder specified by `--temp-path`, where compiled scripts and includes are copied. BSArch uses this path to build a BSA/BA2 package.


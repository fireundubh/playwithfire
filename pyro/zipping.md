---
title: Zipping
description: 
published: true
date: 2021-06-14T12:15:59.247Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:11:05.912Z
---

Pyro can create ZIP archives containing any files defined in the `ZipFile` node block.


# Defining ZIP Files

To configure the ZIP archive:

1. Add the `Zip` attribute to the `PapyrusProject` node. Set the value to `True`.
2. Add a `ZipFiles` block with as many `ZipFile` child blocks as needed.
3. Each `ZipFile` block can contain as many `Include` and `Match` nodes as needed.


## Example

```xml
<ZipFiles Output="@OutputPath">
  <ZipFile Name="@ModName" RootDir="@OutputPath" Compression="deflate">
    <Include NoRecurse="true">MyPlugin.esp</Include>
    <Include NoRecurse="true">MyPlugin.bsa</Include>
    <Match In="SKSE">*.dll</Match>
    <Match In="Strings">*.*strings</Match>
  </ZipFile>
  <ZipFile Name="@ModName - English" RootDir="@OutputPath" Compression="deflate">
    <Match In="Strings">*.*strings</Match>
  </ZipFile>
</ZipFiles>
```


# Including files

Files can be included in ZIP archives using both `Include` and `Match` nodes.

- The `Include` node supports relative file and folder paths, absolute file and folder paths, and glob expressions.
- The `Match` node supports wildcard file patterns, including file negation and directory exclusion patterns.

All matches are case insensitive. Files can be matched outside the project root but are added to the root of ZIP archives by default.


## Using the Include node

```xml
<!-- Search for pattern "README.md" from the project path, recursively if not found in the project root -->
<Include NoRecurse="false">README.md</Include>

<!-- Like above but adds the "README.md" file to the "docs" folder in the ZIP archive -->
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
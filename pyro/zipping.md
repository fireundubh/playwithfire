---
title: Zipping
description: 
published: true
date: 2021-06-13T12:28:08.501Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:11:05.912Z
---

Pyro can create ZIP archives containing any files defined in the `ZipFile` node block.


# Configuring ZIP archives

To configure the ZIP archive:

1. Add the `Zip` attribute to the `PapyrusProject` node. Set the value to `true`.
2. Add a `ZipFiles` node.
3. Add `ZipFile` child nodes to `ZipFiles`, defining `Include` nodes for each `ZipFile`.

See below:

```xml
<ZipFiles Output="{relative or absolute path to output folder where ZIP files will be written}">
  <ZipFile
    Name="{file name}"
    RootDir="{required - relative or absolute path to folder containing files or folders to include}"
    Compression="{choices: 'store' or 'deflate' compression}">
    <Include>{relative or absolute path to file or folder in RootDir, or simple glob pattern}</Include>
    <Include>MyProject.esp</Include>
    <Include NoRecurse="true">*.bsa</Include>
    <Include Path="optional">MyProject - Optional Patch.esp</Include>
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
<!-- Search for pattern "readme.md" from the project path, recursively if not found in the project root -->
<Include NoRecurse="false">README.md</Include>

<!-- Like above but adds the "README.md" file to the "docs" folder in the ZIP archive -->
<Include Path="docs">README.md</Include>

<!-- Search for pattern "docs\readme.md" from the project path, recursively if not found from the project root -->
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
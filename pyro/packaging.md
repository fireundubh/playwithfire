---
title: Packaging
description: 
published: true
date: 2021-06-14T12:05:51.546Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:10:18.847Z
---

You can package scripts and other files into BSA and BA2 archives with [BSArch](https://www.nexusmods.com/newvegas/mods/64745), of which the latest unmodified version is included with Pyro under the MPL 2.0 license.

# Installing BSArch

To install BSArch:

1. If, for some reason, BSArch is not located in the `pyro\tools` folder, download BSArch from the above URL and extract the executable there.
2. The path to `bsarch.exe` should be automatically detected. If not, use the `--bsarch-path` argument to set the path.

# Configuring Packages

To configure packages:

1. Add the `Package` attribute to the `PapyrusProject` node. Set the value to `true`.
2. Add a `Packages` node block, defining as many `Package` nodes as needed. See below:

```xml
<Packages Output="{relative or absolute path to output folder where BSA/BA2 packages will be written}">
  <Package Name="{file name}" RootDir="{required - relative or absolute path to folder containing files or folders to include}">
    <Include>{relative or absolute path to file or folder in RootDir, or simple glob pattern}</Include>
    <Include NoRecurse="true">scripts</Include>
    <Include NoRecurse="false">**/*.txt</Include>
  </Package>
  <Package Name="{file name}" RootDir="{required - relative or absolute path to folder containing includes}">
    <Include NoRecurse="false">**/*.dds</Include>
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


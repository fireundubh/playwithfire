---
title: Zipping
description: 
published: true
date: 2021-05-30T23:11:05.912Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:11:05.912Z
---

Pyro can create ZIP archives containing any files defined in the `ZipFile` node block.

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


---
title: Divine CLI
description: 
published: true
date: 2020-10-30T23:12:37.437Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:05:28.715Z
---

# Required Arguments

Short | Long | Allowed Values | Description
 :--- | :--- | :--- | :---
 `-g` | `--game` | <ul><li>`bg3`</li><li>`dos`<li>`dosee`<li>`dos2` (default)<li>`dos2de`</ul> | Set target game when generating output
`-s` | `--source` | `(absolute file/folder path)` | Set source file path or directory
`-a` | `--action` | <ul><li>`create-package`<li>`list-package`<li>`extract-package` (default)<li>`convert-model`<li>`convert-resource`<li>`extract-packages`<li>`convert-models`<li>`convert-resources`</ul> | Set action to execute

# Optional Arguments

Short | Long | Allowed Values | Description
:--- | :--- | :--- | :---
`-l` | `--loglevel` | <ul><li>`off`<li>`fatal`<li>`error`<li>`warn`<li>`info` (default)<li>`debug`<li>`trace`<li>`all`</ul> | Set verbosity level of log output
`-d` | `--destination` | `(absolute file/folder path)` | Set destination file path or directory
`-i` | `--input-format` | <ul><li>`dae`<li>`gr2`<li>`lsv`<li>`pak`<li>`lsj`<li>`lsx`<li>`lsb`<li>`lsf`</ul> | Set input format for batch actions
`-o` | `--output-format` | <ul><li>`dae`<li>`gr2`<li>`lsv`<li>`pak`<li>`lsj`<li>`lsx`<li>`lsb`<li>`lsf`</ul> | Set output format for batch actions
`-c` | `--compression-method` | <ul><li>`zlib`<li>`zlibfast`<li>`lz4`<li>`lz4hc` (default)<li>`none`</ul> | Set compression method
`-e` | `--gr2-options` | <ul><li>`export-normals`<li>`export-tangents`<li>`export-uvs`<li>`export-colors`<li>`deduplicate-vertices`<li>`deduplicate-uvs`<li>`recalculate-normals`<li>`recalculate-tangents`<li>`recalculate-iwt`<li>`flip-uvs`<li>`ignore-uv-nan`<li>`y-up-skeletons`<li>`force-legacy-version`<li>`compact-tris`<li>`build-dummy-skeleton`<li>`apply-basis-transforms`<li>`x-flip-skeletons`<li>`x-flip-meshes`<li>`conform`<li>`conform-copy`</ul> | Set extra options for GR2/DAE conversion
`-x` | `--expression` | `(string)` | Set glob expression for extract and list actions

# Optional Switch Arguments

Long | Description
:--- | :---
`--conform-path` | Set conform to original path
`--use-package-name` | Use package name for destination folder
`--use-regex` | Use Regular Expressions for expression type
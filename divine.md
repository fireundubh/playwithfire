---
title: Divine CLI
description: 
published: true
date: 2020-10-30T23:20:37.974Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:05:28.715Z
---

# Arguments

## Required Arguments

```
  -g, --game                       Target game when generating output
    Allowed Values:
      dos, dosee, dos2, dos2de, bg3

  -s, --source                     Source file path or directory

  -a, --action                     Action to execute
    Allowed Values:
      create-package, list-package, extract-single-file, extract-package,
      extract-packages, convert-model, convert-models, convert-resource,
      convert-resources
```

## Optional Arguments
```
  -l, --loglevel                   Log output verbosity
    Default Value:
      info
    Allowed Values:
      off, fatal, error, warn, info, debug, trace, all

  -d, --destination                Destination file path or directory

  -f, --packaged-path              File to extract from package

  -i, --input-format               Input format for batch operations
    Allowed Values:
      dae, gr2, lsv, pak, lsj, lsx, lsb, lsf

  -o, --output-format              Output format for batch operations
    Allowed Values:
      dae, gr2, lsv, pak, lsj, lsx, lsb, lsf

  -c, --compression-method         Compression method
    Default Value:
      lz4hc
    Allowed Values:
      zlib, zlibfast, lz4, lz4hc, none

  -e, --gr2-options                Extra options for GR2/DAE conversion
    Allowed Values:
      export-normals, export-tangents, export-uvs, export-colors,
      deduplicate-vertices, deduplicate-uvs, recalculate-normals,
      recalculate-tangents, recalculate-iwt, flip-uvs, ignore-uv-nan,
      y-up-skeletons, force-legacy-version, compact-tris, build-dummy-skeleton,
      apply-basis-transforms, x-flip-skeletons, x-flip-meshes, conform,
      conform-copy

  -x, --expression                 Glob expression for extract and list actions
```

## Optional Switch Arguments
```
  --conform-path                   Conform to original path

  --use-package-name               Use package name for destination folder

  --use-regex                      Use Regular Expressions for expression type
```
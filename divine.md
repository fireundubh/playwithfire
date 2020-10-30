---
title: Divine CLI
description: 
published: true
date: 2020-10-30T23:43:19.456Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:05:28.715Z
---

# Usage

> All paths should be absolute (full) paths.
{.is-warning}


## Conversion

### Convert Model

```
divine -g {game} -s {path to file} -d {path to output file} -a convert-model -e {values}
```

#### Batch Action: Convert Models

```
divine -g {game} -s {path to folder} -d {path to output folder} -a convert-models -e {values} -i {format} -o {format}
```

### Convert Resource

```
divine -g {game} -s {path to file} -d {path to output file} -a convert-resource
```

#### Batch Action: Convert Resources

```
divine -g {game} -s {path to folder} -d {path to output folder} -a convert-resources -i {format} -o {format}
```


## Packages

### Create Package

```
divine -g {game} -s {path to folder} -d {path to output file} -a create-package
```

### List Package

```
divine -g {game} -s {path to PAK} -a list-package
```

### Extract Single File

```
divine -g {game} -s {path to PAK} -d {file name or path in PAK} -a extract-single-file
```

### Extract Package (default)

Extract contents of PAK to "destination path":
```
divine -g {game} -s {path to PAK} -d {path to folder}
```

Extract contents of PAK to "destination path\package name":
```
divine -g {game} -s {path to PAK} -d {path to folder} --use-package-name
```

### Extract Packages

Extract contents of all PAKs to "destination path":
```
divine -g {game} -s {path to folder} -d {path to folder} -a extract-packages
```

Extract contents of all PAKs to "destination path\package name":
```
divine -g {game} -s {path to folder} -d {path to folder} -a extract-packages --use-package-name
```



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
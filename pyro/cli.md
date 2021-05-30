---
title: Command Line Arguments
description: 
published: true
date: 2021-05-30T23:20:13.376Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:20:13.376Z
---


```
--------------------------------------------------------------------------------
                                   P  Y  R  O                                   
----------------------------------------------------- github.com/fireundubh/pyro

usage: pyro.exe [input_path] [options]

required arguments:
  input_path              relative or absolute path to file
                          (if relative, must be relative to current working directory)

build arguments:
  --ignore-errors         ignore compiler errors during build
  --no-implicit-imports   do not build with implicit imports
  --no-incremental-build  do not build incrementally
  --no-parallel           do not parallelize compilation
  --worker-limit          max workers for parallel compilation
                          (usually set automatically to processor count)

compiler arguments:
  --compiler-path         relative or absolute path to PapyrusCompiler.exe
                          (if relative, must be relative to current working directory)
  --flags-path            relative or absolute path to Papyrus Flags file
                          (if relative, must be relative to project)
  --output-path           relative or absolute path to output folder
                          (if relative, must be relative to project)

game arguments:
  -g, --game-type         set game type {fo4, tes5, sse}
  --game-path             relative or absolute path to game install directory
                          (if relative, must be relative to current working directory)
  --registry-path         path to Installed Path key in Windows Registry

bsarch arguments:
  --bsarch-path           relative or absolute path to bsarch.exe
                          (if relative, must be relative to current working directory)
  --package-path          relative or absolute path to bsa/ba2 output folder
                          (if relative, must be relative to project)
  --temp-path             relative or absolute path to temp folder
                          (if relative, must be relative to current working directory)

zip arguments:
  --zip-compression       set compression method {store, deflate}
  --zip-output-path       relative or absolute path to zip output folder
                          (if relative, must be relative to project)

remote arguments:
  --access-token          access token for GitHub remotes
                          (must have public_repo access scope)
  --force-overwrite       download remote files and overwrite existing files
                          (default: skip download when remote folder exists)
  --remote-temp-path      relative or absolute path to temp folder for remote files
                          (if relative, must be relative to project)

debugging arguments:
  --resolve-ppj           resolve variables and paths in ppj file

program arguments:
  --help                  show help and exit
```

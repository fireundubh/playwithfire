---
title: Pyro
description: 
published: true
date: 2020-10-28T07:02:48.568Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:04:59.413Z
---

**Pyro** is a parallelized incremental build system for _Skyrim Classic_ (TES5), _Skyrim Special Edition_ (SSE), and _Fallout 4_ (FO4) projects.

Pyro provides mod authors with an all-in-one tool for compiling Papyrus scripts, packaging BSA and BA2 archives, and preparing builds for distribution.

Pyro can be integrated as an external tool into any IDE, allowing mod authors to "Instant Build" projects with a single hotkey.

# What's New?

See: [Release Notes](/pyro/release-notes)

# Binaries

Latest build from master branch:

[![](https://github.com/fireundubh/pyro/workflows/GitHub%20CI/badge.svg)](https://github.com/fireundubh/pyro/actions)

Latest pre-release binaries:

Source | Comments
:--- | :---
[GitHub Releases](https://github.com/fireundubh/pyro/releases) | Always up-to-date; builds intended for most users.
[GitHub CI](https://github.com/fireundubh/pyro/actions) | Bleeding edge; builds intended for testing; not for most users.
[SSE Nexus](https://www.nexusmods.com/skyrimspecialedition/mods/35860) | Mirror for GitHub Releases; may lag behind.

Or build Pyro from the source code. Refer to the [Compiling](#compiling) section for details.

## Integrations

[Papyrus Language Tools for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=joelday.papyrus-lang-vscode) by Joel Day (ispillmydrink)<br>[![](https://github.com/joelday/papyrus-lang/workflows/GitHub%20CI%3A%20Dev%20Build/badge.svg)](https://github.com/joel-day/papyrus-lang/actions) [![](https://github.com/joelday/papyrus-lang/workflows/GitHub%20CI%3A%20Release%20Build/badge.svg)](https://github.com/joel-day/papyrus-lang/actions)

**Note:** Papyrus Language Tools v2.21.2 uses an older build of Pyro, dated 2019-11-26. There have been at least 12 new builds since.

# Features

## Overview

- Pyro brings the [Papyrus Projects (PPJ)](https://www.creationkit.com/fallout4/index.php?title=Papyrus_Projects) system to TES5 and SSE and extends the schema for FO4.
- Pyro introduces the first incremental build system for TES5, SSE, and FO4 projects, significantly accelerating compilation, testing, and deployment.
- Pyro parallelizes compilation, taking advantage of multi-core processors to compile multiple scripts simultaneously.
- Pyro anonymizes compiled Papyrus scripts, removing identifying metadata embedded by the Papyrus Compiler.
- Pyro automatically creates multiple BSA and BA2 packages using [BSArch](https://www.nexusmods.com/newvegas/mods/64745).
- Pyro automatically creates ZIP archives of customizable collections of files.
- Pyro supports importing and compiling from GitHub repositories and public Bitbucket Cloud repositories.
- Pyro supports variable substitution in Papyrus Projects, including environment and user variables.



## Multiple Game Support

Pyro supports each version of the Papyrus Compiler for _Skyrim Classic_ (TES5), _Skyrim Special Edition_ (SSE), and _Fallout 4_ (FO4).

There are multiple ways to change the compiler version:

1. Use the `-g, --game-type` argument to specify one of these games: `fo4`, `sse`, or `tes5`.
2. Use the `--game-path` argument to specify the path to where one of the above games is installed.
3. Use the `--registry-path` argument to specify the path to the `Installed Path` key in the Windows Registry for the respective game.
4. Add the `Game` attribute to the `<PapyrusProject>` element in your Papyrus Project file with one of these values: `fo4`, `sse`, or `tes5`.


## Extended Schema

> Refer to the [Pyro Project Schema](/pyro/schema) page for default attribute values.

> Refer to the [Pyro Project XML Schema Definition](https://github.com/fireundubh/pyro/blob/master/pyro/PapyrusProject.xsd) for document structure, type constraints, and other rules.

Bethesda Game Studios introduced the PPJ schema with the Papyrus Compiler for FO4. The TES5 and SSE compilers do not support the schema.

Pyro supports all standard PPJ elements and attributes used by the Papyrus Compiler. The PPJ schema has also been extended to support features unique to Pyro.

**Note:** The `Asm` attribute of the `PapyrusProject` node is ignored by Pyro. The Papyrus Compiler uses this attribute to call the Papyrus Assembler but generating assembly files for Papyrus scripts is out-of-scope for Pyro.


## Incremental Build with Parallelized Compilation

Incremental build _vastly_ accelerates builds by compiling only scripts that *need* to be compiled. Pyro determines which PSC files to compile by comparing the last modified timestamp on PSC files with the compilation timestamps embedded in PEX files. Pyro then spawns multiple workers (compiler instances) in parallel to further reduce build times.

Each instance of the compiler will be executed with "below normal" priority, allowing you to continue working without the Papyrus Compiler significantly impacting the performance of your system.


## Anonymization

When the Papyrus Compiler compiles a script, your system username, your computer name's on your local network, and the full path to the source script are embedded in the header. This data can be retrieved using a hex editor or a Papyrus decompiler, such as Champollion. This data could put at risk your security or privacy. Pyro replaces those strings in compiled scripts with random letters.

Simply add the `Anonymize` attribute to the `PapyrusProject` node and set the value to `True`.


## Packaging

You can package scripts and other files into BSA and BA2 archives with [BSArch](https://www.nexusmods.com/newvegas/mods/64745), of which the latest unmodified version is included with Pyro under the MPL 2.0 license.

### Installing BSArch

To install BSArch:

1. If, for some reason, BSArch is not located in the `pyro\tools` folder, download BSArch from the above URL and extract the executable there.
2. The path to `bsarch.exe` should be automatically detected. If not, use the `--bsarch-path` argument to set the path.

### Configuring Packages

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

### Temporary files

The packaging system uses a default temporary folder, or a folder specified by `--temp-path`, where compiled scripts and includes are copied. BSArch uses this path to build a BSA/BA2 package.


## Zipping

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
  </ZipFile>
</ZipFiles>
```


## Remotes

Pyro can import and download scripts from GitHub and public Bitbucket Cloud repositories.

### Importing scripts

When a GitHub or public Bitbucket Cloud URL is used as an `Import` path, Pyro will download the respective files and use the download location as the import path.

For example:

```xml
<Imports>
  <!-- Pyro will accept a GitHub page address. -->
  <Import>https://github.com/fireundubh/skyui/tree/master/dist/Data/Scripts/Source</Import>
  <!-- Pyro will also accept a GitHub API address. -->
  <Import>https://api.github.com/repos/fireundubh/skyui/contents/dist/Data/Scripts/Source?ref=master</Import>
</Imports>
```

### Compiling scripts

When a GitHub or public Bitbucket Cloud URL is used as an `Folder` path, Pyro will download the respective files and use the download location as the folder path.

For example:

```xml
<Folders>
  <!-- Pyro will accept a GitHub page address. -->
  <Folder NoRecurse="false">https://github.com/chesko256/Campfire/tree/master_fo4/Scripts/Source</Folder>
  <!-- Pyro will also accept a GitHub API address. -->
  <Folder NoRecurse="false">https://api.github.com/repos/chesko256/Campfire/contents/Scripts/Source?ref=master_fo4</Folder>
</Folders>
```

If the `NoRecurse` attribute is set to `true`, all remote files will still be downloaded but only scripts in the initial folder will be compiled.


### Configuring remotes

The following arguments support remotes:

Argument | Required | Description | Type | Default Value
:--- | :--- | :--- | :--- | :---
`--access-token` | `true`<br>(when using GitHub remotes) | [your personal access token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line)<br>(must have `public_repo` access scope) | `str` | 
`--force-overwrite` | `false` | download remote files and overwrite existing files<br>(default: skip download when remote folder exists) | `bool` | `false`
`--remote-temp-path` | `false` | relative or absolute path to temp folder for remote files<br>(if relative, must be relative to project) | `str` | `{program_path}\remote`

Public Bitbucket Cloud repositories do not require an access token.

To use GitHub repositories, the `--access-token` argument must be provided. 


## Variables

Pyro can substitute variables with defined values in PPJ paths and string attributes.

To configure variables:

1. Add a `Variables` node block.
2. Add as many `Variable` nodes to that block as needed.

For example:

```xml
<Variables>
  <Variable Name="namespace" Value="Master of Disguise"/>
  <Variable Name="modname" Value="Master of Disguise - Special Edition"/>
  <Variable Name="myproject" Value="E:\projects\skyrim\Master of Disguise - Special Edition"/>
</Variables>
```

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

In addition, regardless of whether a `Variables` node group is defined, environment variables (e.g., `%APPDATA%`) and user variables (`~user`) will also be expanded.


## Build Events

Build events are sequences of shell commands that execute before and after the project builds.

Pyro supports pre-build events and post-build events.


### Options

The `PreBuildEvent` and `PostBuildEvent` elements have the following attributes:

- A `Description` attribute can be used to clarify each event to the user. This description will also be logged in the build output.
- A `UseInBuild` attribute can be used to toggle whether the event is used.

The `Command` element does not have any attributes.

### Timing

Event | Runs When
:--- | :---
PRE | Immediately prior to compilation
POST | Immediately after build success


### Examples

```xml
<PreBuildEvent Description="Pre-Build Event Example" UseInBuild="true">
  <Command>echo Hi! I'm a pre-build command!</Command>
</PreBuildEvent>
```

```xml
<PostBuildEvent Description="Post-Build Event Example" UseInBuild="true">
  <Command>echo Hi! I'm a post-build command!</Command>
</PostBuildEvent >
```


# Command Line Arguments

```
--------------------------------------------------------------------------------
                                   P  Y  R  O                                   
----------------------------------------------------- github.com/fireundubh/pyro

usage: pyro.exe [--ignore-errors] [--no-incremental-build] [--no-parallel]
                [--worker-limit] [--compiler-path] [--flags-path]
                [--output-path] [-g {fo4,tes5,sse}]
                [--game-path  | --registry-path ] [--bsarch-path]
                [--package-path] [--temp-path]
                [--zip-compression {store,deflate}] [--zip-output-path]
                [--access-token] [--force-overwrite] [--remote-temp-path]
                [--resolve-ppj] [--log-path] [--help]
                [input_path]

required arguments:
  input_path              relative or absolute path to file
                          (if relative, must be relative to current working directory)

build arguments:
  --ignore-errors         ignore compiler errors during build
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
  -g, --game-type         set game type (choices: fo4, tes5, sse)
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
  --zip-compression       set compression method (choices: store, deflate)
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
  --log-path              relative or absolute path to log folder
                          (if relative, must be relative to current working directory)

program arguments:
  --help                  show help and exit
```


# Resources

## Example PPJs

* [Auto Loot.ppj](https://gist.github.com/fireundubh/7eecf97135b8da74e59133842f0b60f9) (Fallout 4)
* [Master of Disguise SSE.ppj](https://gist.github.com/fireundubh/cb3094ed851f74326090a681a78d5c5e) (Skyrim Special Edition)


# Contributing

## Compiling

### Install Pipenv

Python | Command | Alternative Command
:--- | :--- | :---
CPython | `pip install pipenv` | `python -m pip install pipenv`
Anaconda | `conda install -c conda-forge pipenv` | &mdash;


### Install Dependencies

1. Change the current working directory (CWD) to the Pyro source folder.
2. Run: `pipenv install`


### Run the Build Script

The build process requires [Nuitka](https://nuitka.net/)  and the [Visual Studio](https://visualstudio.microsoft.com/downloads/) build tools. Nuitka was installed in the previous step.

Using the Developer Command Prompt for Visual Studio, change the CWD to the Pyro source folder and run:

Command | Alternative Command
:--- | :---
`python build.py` | `pipenv run python build.py`

Executing the build script will create a `pyro.dist` directory that contains the executable and required libraries and modules. A ZIP archive will be created in the `bin` folder.


### Optional Build Script Arguments

The build script has three arguments.

Short Argument | Long Argument |  Help
:--- | :--- | :---
&mdash; | `--no-zip` | Skips ZIP generation. Useful for CI.
&mdash; | `--vcvars64-path` | Path to Visual Studio Developer Command Prompt (x64)


# Licenses

Pyro is open source and licensed under the MIT License.

BSArch is licensed under the MPL 2.0 license. The binary bundled with Pyro was compiled from the original unmodified source code available [here](https://github.com/ElminsterAU/xEdit/tree/master/Tools/BSArchive).


# Credits

* fireundubh (lead developer)
* rjstone (contributor)
* xnyo (contributor)
* Scrivener07 (tester)
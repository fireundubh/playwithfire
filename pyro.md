<!-- TITLE: Pyro -->

# Pyro

**Pyro** is a parallelized incremental build system for _Skyrim Classic_ (TESV), _Skyrim Special Edition_ (SSE), and _Fallout 4_ (FO4) projects.

Pyro provides mod authors with an all-in-one tool for compiling Papyrus scripts, packaging BSA and BA2 archives, and preparing builds for distribution.

Pyro can be integrated as an external tool into any IDE, allowing mod authors to "Instant Build" projects with a single hotkey.

## Contents

- [Features](#features)
  - [Overview](#overview)
  - [Multiple Game Support](#multiple-game-support)
  - [Extended PPJ Format](#extended-papyrus-project-format)
  - [Incremental Build with Parallelized Compilation](#incremental-build-with-parallelized-compilation)
  - [Anonymization](#anonymization)
  - [Packaging](#packaging)
  - [Zipping](#zipping)
  - [Variables](#variables)
  - [Remotes](#remotes)
- [Command Line Arguments](#command-line-arguments)
- [Resources](#resources)
  - [Example PPJs](#example-pp-js)
- [Contributing](#contributing)
  - [License](#license)
  - [Compiling](#compiling)

## Binaries

Latest build from master branch:

[![](https://github.com/fireundubh/pyro/workflows/GitHub%20CI/badge.svg)](https://github.com/fireundubh/pyro/actions)

Latest pre-release binaries:

[GitHub Releases](https://github.com/fireundubh/pyro/releases)

Or build Pyro from the source code. Refer to the [Compiling](#compiling) section for details.

## Features

### Overview

- Pyro brings the [Papyrus Project (PPJ) format](https://www.creationkit.com/fallout4/index.php?title=Papyrus_Projects) to TESV and SSE and expands on the format for FO4.
- Pyro introduces the first incremental build system for TESV, SSE, and FO4 projects, significantly accelerating compilation, testing, and deployment.
- Pyro parallelizes compilation, taking advantage of multi-core processors to compile multiple scripts simultaneously.
- Pyro can anonymize compiled Papyrus scripts, removing identifying metadata embedded by the Papyrus Compiler.
- Pyro can automatically create multiple BSA and BA2 packages using [BSArch](https://www.nexusmods.com/newvegas/mods/64745).
- Pyro can automatically create a ZIP archive of user-defined files.
- Pyro supports variable substitution in Papyrus Projects.
- Pyro supports importing and compiling from GitHub repositories.


### Multiple Game Support

Pyro supports each version of the Papyrus Compiler for _Skyrim Classic_ (TESV), _Skyrim Special Edition_ (SSE), and _Fallout 4_ (FO4).

There are multiple ways to change the compiler version:

1. Use the `-g, --game-type` argument to specify one of these games: `fo4`, `sse`, or `tesv`.
2. Use the `--game-path` argument to specify the path to where one of the above games is installed.
3. Use the `--registry-path` argument to specify the path to the `Installed Path` key in the Windows Registry for the respective game.
4. Add the `Game` attribute to the `<PapyrusProject>` element in your Papyrus Project file with one of these values: `fo4`, `sse`, or `tesv`.


### Extended Papyrus Project Format

Bethesda Game Studios introduced the PPJ format with the Papyrus Compiler for FO4. The TESV and SSE compilers do not support the format.

Pyro supports all standard PPJ elements and attributes used by the Papyrus Compiler. The PPJ format has also been extended to support features unique to Pyro. For details, refer to Pyro's [Papyrus Project XML Schema Definition](https://github.com/fireundubh/pyro/blob/master/pyro/PapyrusProject.xsd).

**Note:** The `Asm` attribute of the `PapyrusProject` node is ignored by Pyro. The Papyrus Compiler uses this attribute to call the Papyrus Assembler but generating assembly files for Papyrus scripts is out-of-scope for Pyro.

#### PapyrusProject Defaults

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`PapyrusProject` | `Game` | `str` | (determined programmatically)
`PapyrusProject` | `Output` | `str` | Path to the `pyro\out` folder
`PapyrusProject` | `Flags` | `str` | (determined programmatically from game path)
`PapyrusProject` | `Optimize` | `bool` | `false`
`PapyrusProject` | `Release` (FO4 only) | `bool` | `false`
`PapyrusProject` | `Final` (FO4 only) | `bool` | `false`
`PapyrusProject` | `Anonymize` | `bool` | `false`
`PapyrusProject` | `Package` | `bool` | `false`

#### Folder Defaults

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Folder` | `NoRecurse` | `bool` | `false`

#### Packages Defaults

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Packages` | `Output` | `str` | Path to the `pyro\dist` folder
`Package` | `Name` | `str` | If the attribute is omitted:<ul><li>the package file will be named after the project,<li>the extension will be appropriate to the game, and<li>subsequent package names will be suffixed with `(1)`, `(2)`, and so on.</ul>
`Package` | `RootDir` | `str` | Path to the project folder 
`Include` | `NoRecurse`  | `bool` | `false`

#### ZipFile Defaults

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`ZipFile` | `Name` | `str` | If the attribute is omitted, the ZIP file will be named after the project.
`ZipFile` | `RootDir` | `str` | Path to the project folder
`ZipFile` | `Output` | `str` | Path to the `pyro\dist` folder
`ZipFile` | `Compression` | `str` | `deflate`
`Include` | `NoRecurse` | `bool` | `false`


### Incremental Build with Parallelized Compilation

Incremental build _vastly_ accelerates builds by compiling only scripts that *need* to be compiled. Pyro determines which PSC files to compile by comparing the last modified timestamp on PSC files with the compilation timestamps embedded in PEX files. Pyro then spawns multiple workers (compiler instances) in parallel to further reduce build times. Each instance of the compiler will be executed with "below normal" priority, allowing you to continue working without the Papyrus Compiler significantly impacting the performance of your system.


### Anonymization

When the Papyrus Compiler compiles a script, your system username, your computer name's on your local network, and the full path to the source script are embedded in the header. This data can be retrieved using a hex editor or a Papyrus decompiler, such as Champollion. This data could put at risk your security or privacy. Pyro replaces those strings in compiled scripts with random letters.

Simply add the `Anonymize` attribute to the `PapyrusProject` node and set the value to `True`.


### Packaging

You can package scripts and other files into BSA and BA2 archives with [BSArch](https://www.nexusmods.com/newvegas/mods/64745), of which the latest unmodified version is included with Pyro under the MPL 2.0 license.

#### Installing BSArch

To install BSArch:

1. If, for some reason, BSArch is not located in the `pyro\tools` folder, download BSArch from the above URL and extract the executable there.
2. The path to `bsarch.exe` should be automatically detected. If not, use the `--bsarch-path` argument to set the path.

#### Configuring Packages

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

#### Temporary files

The packaging system uses a default temporary folder, or a folder specified by `--temp-path`, where compiled scripts and includes are copied. BSArch uses this path to build a BSA/BA2 package.


### Zipping

Pyro can create a ZIP archive containing any files defined in the `ZipFile` node block.

#### Configuring ZipFile

To configure the ZIP archive:

1. Add the `Zip` attribute to the `PapyrusProject` node. Set the value to `true`.
2. Add a `ZipFile` node block, defining as many `Include` nodes as needed. See below:

```xml
<ZipFile
  Name="{file name}"
  RootDir="{required - relative or absolute path to folder containing files or folders to include}"
  Output="{relative or absolute path to output folder where ZIP file will be written}"
  Compression="{choices: 'store' or 'deflate' compression}">
  <Include>{relative or absolute path to file or folder in RootDir, or simple glob pattern}</Include>
  <Include>MyProject.esp</Include>
  <Include NoRecurse="true">*.bsa</Include>
</ZipFile>
```


### Variables

Pyro can substitute variables with defined values in PPJ paths and string attributes.

#### Configuring Variables

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
<ZipFile Name="@modname" RootDir="@myproject" Output="@myproject" Compression="deflate">
  <Include>@myproject\@modname.esp</Include>
  <Include NoRecurse="true">*.bsa</Include>
</ZipFile>
```

Pyro will expand those variables when the project is loaded.


### Remotes

Pyro can import and download scripts from GitHub repositories.

#### Importing scripts from remotes

When a GitHub URL is used as an `Import` path, Pyro will download the respective files and use the download location as the import path.

For example:

```xml
<Imports>
  <!-- Pyro will accept a GitHub page address. -->
  <Import>https://github.com/fireundubh/skyui/tree/master/dist/Data/Scripts/Source</Import>
  <!-- Pyro will also accept a GitHub API address. -->
  <Import>https://api.github.com/repos/fireundubh/skyui/contents/dist/Data/Scripts/Source?ref=master</Import>
</Imports>
```

#### Compiling scripts from remotes

When a GitHub URL is used as an `Folder` path, Pyro will download the respective files and use the download location as the folder path.

For example:

```xml
<Folders>
  <!-- Pyro will accept a GitHub page address. -->
  <Folder>https://github.com/fireundubh/skyui/tree/master/dist/Data/Scripts/Source</Import>
  <!-- Pyro will also accept a GitHub API address. -->
  <Folder>https://api.github.com/repos/fireundubh/skyui/contents/dist/Data/Scripts/Source?ref=master</Import>
</Folders>
```

#### Configuring remote support

To use GitHub repositories, the `--access-token` argument must be provided. The following arguments support remotes.

Argument | Required | Description | Type | Default Value
:--- | :--- | :--- | :--- | :---
`--access-token` | `true` (when using remotes) | [your personal access token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line)<br>(must have `public_repo` access scope) | `str` | 
`--force-overwrite` | `false` | download remote files and overwrite existing files<br>(default: skip download when remote folder exists) | `bool` | `false`
`--remote-temp-path` | `false` | relative or absolute path to temp folder for remote files<br>(if relative, must be relative to project) | `str` | `{program_path}\remote`


## Command Line Arguments

```
--------------------------------------------------------------------------------
                                   P  Y  R  O
----------------------------------------------------- github.com/fireundubh/pyro

usage: pyro [-i] [--ignore-errors] [--no-incremental-build] [--no-parallel]
            [--worker-limit] [--compiler-path] [--flags-path] [--output-path]
            [-g {tesv,fo4,sse}] [--game-path  | --registry-path ]
            [--bsarch-path] [--package-path] [--temp-path]
            [--zip-compression {store,deflate}] [--zip-output-path]
            [--access-token] [--force-overwrite] [--remote-temp-path]
            [--resolve-ppj] [--log-path] [--help]

required arguments:
  -i, --input-path        relative or absolute path to file
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
  -g, --game-type         set game type (choices: fo4, tesv, sse)
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
  --access-token          personal access token
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


## Resources

### Example PPJs

* [Auto Loot.ppj](https://gist.github.com/fireundubh/7eecf97135b8da74e59133842f0b60f9) (Fallout 4)
* [Master of Disguise SSE.ppj](https://gist.github.com/fireundubh/cb3094ed851f74326090a681a78d5c5e) (Skyrim Special Edition)


## Contributing

### Compiling

#### Install Pipenv

Python | Command | Alternative Command
:--- | :--- | :---
CPython | `pip install pipenv` | `python -m pip install pipenv`
Anaconda | `conda install -c conda-forge pipenv` | &mdash;


#### Install Dependencies

1. Change the current working directory (CWD) to the Pyro source folder.
2. Run: `pipenv install`


#### Run the Build Script

The build process requires [Nuitka](https://nuitka.net/)  and the [Visual Studio](https://visualstudio.microsoft.com/downloads/) build tools. Nuitka was installed in the previous step.

Using the Developer Command Prompt for Visual Studio, change the CWD to the Pyro source folder and run:

Command | Alternative Command
:--- | :---
`python build.py` | `pipenv run python build.py`

Executing the build script will create a `pyro.dist` directory that contains the executable and required libraries and modules. A ZIP archive will be created in the `bin` folder.


##### Build Script

The build script has three arguments.

Short Argument | Long Argument |  Help
:--- | :--- | :---
&mdash; | `--no-zip` | Skips ZIP generation. Useful for CI.
&mdash; | `--vcvars64-path` | Path to Visual Studio Developer Command Prompt (x64)


### Licenses

Pyro is open source and licensed under the MIT License.

BSArch is licensed under the MPL 2.0 license. The binary bundled with Pyro was compiled from the original unmodified source code available [here](https://github.com/ElminsterAU/xEdit/tree/master/Tools/BSArchive).


### Credits

* fireundubh (lead developer)
* rjstone (contributor)
* xnyo (contributor)
<!-- TITLE: Pyro -->

# Pyro

**Pyro** is a parallelized incremental build system for _Skyrim Classic_ (TESV), _Skyrim Special Edition_ (SSE), and _Fallout 4_ (FO4) projects. Pyro provides mod authors with an all-in-one tool for compiling Papyrus scripts, packaging BSA and BA2 archives, and preparing builds for distribution. Pyro can be integrated as an external tool into any IDE, allowing mod authors to "Instant Build" projects with a single hotkey.

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
- [Resources](#resources)
  - [Example PPJ Files](#example-ppj-files)
  - [IDE Integration](#ide-integration)
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

- Pyro brings [Papyrus Projects](https://www.creationkit.com/fallout4/index.php?title=Papyrus_Projects) to Skyrim and expands on the existing system for Fallout 4.
- Pyro introduces the first incremental build system for Skyrim and Fallout 4 projects, significantly accelerating compilation, testing, and deployment.
- Pyro parallelizes compilation, taking advantage of multi-core processors to compile multiple scripts simultaneously.
- Pyro can anonymize compiled Papyrus scripts, removing identifying metadata added by the Papyrus Compiler.
- Pyro can automatically create multiple BSA and BA2 packages using [BSArch](https://www.nexusmods.com/newvegas/mods/64745).
- Pyro can automatically create a ZIP archive of user-defined files.
- Pyro supports variable substitution in Papyrus Projects.


### Multiple Game Support

Pyro supports each version of the Papyrus Compiler for _Skyrim Classic_ (TESV), _Skyrim Special Edition_ (SSE), and _Fallout 4_ (FO4).

There are multiple ways to change the compiler version:

1. Use the `-g, --game-type` argument to specify one of these games: `fo4`, `sse`, or `tesv`.
2. Use the `--game-path` argument to specify the path to where one of the above games is installed.
3. Use the `--registry-path` argument to specify the path to the `Installed Path` key in the Windows Registry for the respective game.
4. Add the `Game` attribute to the `<PapyrusProject>` element in your Papyrus Project file with one of these values: `fo4`, `sse`, or `tesv`.


### Extended Papyrus Project Format

Bethesda Game Studios introduced the Papyrus Project (PPJ) format with the Papyrus Compiler for *Fallout 4*. The compilers for _Skyrim Classic_ and _Skyrim Special Edition_ do not support the format.

Pyro supports all PPJ elements and attributes used by the Papyrus Compiler. The PPJ format has also been extended to support features unique to Pyro. For details, refer to Pyro's [Papyrus Project XML Schema Definition](https://github.com/fireundubh/pyro/blob/master/pyro/PapyrusProject.xsd).

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

Incremental build _vastly_ accelerates builds by compiling only scripts that need to be compiled. The incremental build system determines which PSC files to compile by comparing the last modified timestamp on PSC files with the compilation timestamps encoded in PEX files by the Papyrus Compiler. Pyro then builds commands to be passed to the Papyrus Compiler and spawn multiple instances of the Papyrus Compiler in parallel to further reduce build times.


#### Benchmarks

The native PPJ compiler for FO4 is on average 70 ms faster per script. Tested with i5-3570k @ 3.4 GHz and 6 scripts.

However, there is no native PPJ compiler for TESV and SSE. Pyro fills that role.


### Anonymization

When the Papyrus Compiler compiles a script is compiled, your system username and computer name are embedded in the header. This data can be easily retrieved using a hex editor or a Papyrus decompiler, such as Champollion. The sharing of this data could put at risk your security or privacy. Pyro replaces those strings in compiled scripts with random letters, effectively anonymizing compiled scripts.

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


## Resources

### Example PPJ Files

* [Auto Loot.ppj](https://gist.github.com/fireundubh/7eecf97135b8da74e59133842f0b60f9)
* [Better Favor Jobs SSE.ppj](https://gist.github.com/fireundubh/398a28227d220f0b45cbdb5fa618b75c)
* [Master of Disguise SSE.ppj](https://gist.github.com/fireundubh/cb3094ed851f74326090a681a78d5c5e)


### IDE Integration

* [PyCharm](https://i.imgur.com/dxk5ZfL.jpg)
* [UltraEdit](https://gist.github.com/fireundubh/cca1f4132ca4b000f094294f3f036fa0)


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
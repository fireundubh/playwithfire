<!-- TITLE: Pyro -->

# Pyro

**Pyro** is a parallelized incremental build system for _Skyrim Classic_ (TESV), _Skyrim Special Edition_ (SSE), and _Fallout 4_ (FO4) projects. Pyro provides mod authors with an all-in-one tool for compiling Papyrus scripts, packaging BSA and BA2 archives, and preparing builds for distribution. Pyro can be integrated as an external tool into any IDE, allowing mod authors to "Instant Build" projects with a single hotkey.

## Binaries

Latest build from master branch:

[![](https://github.com/fireundubh/pyro/workflows/GitHub%20CI/badge.svg)](https://github.com/fireundubh/pyro/actions)

Or build Pyro from source. Refer to the [Compiling](#compiling) section for details.

## Features

### Overview

- Pyro brings [Papyrus Projects](https://www.creationkit.com/fallout4/index.php?title=Papyrus_Projects) to Skyrim and expands on the existing system for Fallout 4.
- Pyro introduces the first incremental build system for Skyrim and Fallout 4 projects, significantly accelerating compilation, testing, and deployment.
- Pyro parallelizes compilation, taking advantage of multi-core processors to compile multiple scripts simultaneously.
- Pyro integrates with [BSArch](https://www.nexusmods.com/newvegas/mods/64745) to automatically package scripts and non-script assets into BSA and BA2 archives.
- Pyro anonymizes compiled Papyrus scripts, removing identifying metadata added by the Papyrus Compiler.


### Multiple Game Support

Pyro supports each version of the Papyrus Compiler for _Skyrim Classic_ (TESV), _Skyrim Special Edition_ (SSE), and _Fallout 4_ (FO4).

There are multiple ways to change the compiler version:

1. Use the `-g, --game-type` argument to specify one of these games: `fo4`, `sse`, or `tesv`.
2. Use the `--game-path` argument to specify the path to where one of the above games is installed.
3. Use the `--registry-path` argument to specify the value of the `Installed Path` key in the Windows Registry for the respective game.
4. Add the `Game` attribute to the `<PapyrusProject>` element in your Papyrus Project file with one of these values: `fo4`, `sse`, or `tesv`.


### Extended Papyrus Project Format

Bethesda Game Studios introduced the Papyrus Project (PPJ) format with the Papyrus Compiler for *Fallout 4*. The compilers for _Skyrim Classic_ and _Skyrim Special Edition_ do not support the format.

Pyro supports all PPJ elements and attributes used by the Papyrus Compiler. The PPJ format has also been extended to support features unique to Pyro. For details, refer to Pyro's [Papyrus Project XML Schema Definition](https://github.com/fireundubh/pyro/blob/master/pyro/PapyrusProject.xsd).

**Note:** The `Asm` attribute of the `PapyrusProject` node is not supported. The Papyrus Compiler uses this attribute to call the Papyrus Assembler but generating assembly files for Papyrus scripts is out-of-scope for Pyro.


### Incremental Build with Parallelized Compilation

Incremental build _vastly_ accelerates builds by compiling only scripts that need to be compiled. The incremental build system determines which PSC files to compile by comparing the last modified timestamp on PSC files with the compilation timestamps encoded in PEX files by the Papyrus Compiler. Pyro then builds commands to be passed to the Papyrus Compiler and spawn multiple instances of the Papyrus Compiler in parallel to further reduce build times.


#### Benchmarks

The native PPJ compiler for FO4 is on average 70 ms faster per script. Tested with i5-3570k @ 3.4 GHz and 6 scripts.

However, there is no native PPJ compiler for TESV and SSE. Pyro fills that role.


### Automatic BSA/BA2 Packaging

You can package scripts into BSA and BA2 archives with [BSArch](https://www.nexusmods.com/newvegas/mods/64745).

1. Copy `bsarch.exe` to the `pyro\tools` folder, if the file does not exist.
2. The path to `bsarch.exe` should be automatically detected. If not, use the `--bsarch-path` argument to set the path.
3. Add the `Archive` attribute to the `PapyrusProject` root element. Set the value to the absolute path to the destination BSA or BA2 archive.
4. Add the `CreateArchive` attribute to the `PapyrusProject` root element. Set the value to `True`.
5. Compile as normal and the compiled scripts will be automatically packaged.

To package arbitrary files, add the following block before the `</PapyrusProject>` end tag:

```xml
<Includes Root="{absolute path to includes root}">
	<Include>{relative path to file in includes root}</Include>
	<Include>{...}</Include>
</Includes>
```

Currently, folder includes are not supported.


#### Notes

* A temporary folder will be created and deleted at a default temporary path or path specified by `--temp-path`.
* The compiled scripts and any arbitrary includes to be packaged will be copied to the temporary folder.
* The temporary folder will be removed if the procedure is successful.


### Script Anonymization

When a script is compiled, your system username and computer name are embedded in the binary header. This information can be revealed with a hex editor or decompiler. If your username is your real name, or you are concerned about targeted attacks using your system login, leaving this information intact can present security and/or privacy risks.

Pyro replaces those strings in compiled scripts with random letters, effectively anonymizing compiled scripts.

Simply add the `Anonymize` attribute to the `PapyrusProject` root element. Set the value to `True`.


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
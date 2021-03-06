---
title: Release Notes
description: 
published: true
date: 2021-06-14T21:14:21.710Z
tags: 
editor: markdown
dateCreated: 2020-05-20T04:28:08.747Z
---

> **Note:** Pre-release version names are Unix timestamps.

# 1623665539

## Major Changes

- Implemented support for parent directory symbol in import paths
- Implemented `Path` attribute of `<Include>` nodes for packages


## Fixes

- Fixed issue where `<PreImportEvent>` and `<PostImportEvent>` nodes were not initialized and parsed
- Fixed issue where `UseInBuild` attribute of event nodes was never checked
- Fixed issue where an invalid wildcard pattern did not cause application to exit with nonzero exit code
- Fixed issue where some relative import and script paths were not handled correctly


# 1623585643

## New Features

Pyro supports the use of `<Match>` nodes to include files in BSA/BA2 packages and ZIP files.

```xml
<Match In="SKSE">*.dll</Match>
```

`<Match>` nodes allow you to use wildcard file patterns, as well as file negation and directory exclusion patterns.

```xml
<Match In="." Exclude="docs" NoRecurse="false">*.md|*.txt|-README*</Match>
```

`<Match>` nodes are distinct from `<Include>` nodes, which use path matching and glob expressions.


## Major Changes

- Implemented folder path support for `<Include>` nodes (e.g., `<Include>Scripts</Include>` would include all files in the `Scripts` folder recursively)
- Allowed files outside project root to be included in ZIP archives
- Reduced time to fail by reordering some project validations before remote downloading


## Fixes

- Fixed issue where some absolute paths in  `<Include>` nodes were not handled correctly
- Fixed issue where some relative paths in  `<Include>` nodes were not handled correctly
- Fixed issue where some info and error log messages were warnings
- Fixed issue where some errors did not cause application to exit with nonzero code


# 1623200029

## Fixes

- Fixed issue where Pyro did not exit with nonzero code on remote failure due to bad request
- Fixed issue where Pyro did not exit with nonzero code on remote failure due to bad response
- Fixed issue where remote failure due to bad request or bad response did not report full status code (e.g., 404 vs 404 Not Found)


# 1622859917

## New Features

- Added support for GitHub clone URLs as remotes (e.g., `https://github.com/fireundubh/LibFire` or `https://github.com/fireundubh/LibFire.git`)
- Added support for current and parent directory symbols in `Folder` paths
- Implemented skipping unchanged files on remotes as default behavior (i.e., only changed files will be downloaded on successive runs unless `--force-overwrite` is passed)


## Fixes

- Fixed issue where application exit code was always zero
- Fixed issue where application did not fail early when flags file was missing from imports
- Fixed issue where files other than Papyrus source and flags files could be downloaded from remotes
- Fixed issue where temp and registry installed paths could be file paths


# 1622420177

## New Features

`PreImportEvent` and `PostImportEvent` elements have been added to the PyroProject XSD. These parent elements contain `Command` children.

> How would these events be useful? In one use case, the user wants to automatically download the latest release of a mod from Nexus Mods, and the user wants to import script sources from that release. Pyro does not support the Nexus API; therefore, the user would need to call an external application to complete the first task, but without the pre-import event, to complete the second task, Pyro would have to become a child of that application's build cycle. With the pre-import event, however, the user can use Pyro to manage calls to that external application.
{.is-info}


### Options

- A `Description` attribute can be used to clarify each event. This description will be printed in the build output.
- A `UseInBuild` attribute can be used to toggle whether the event is used.


### Timing

Event | Runs When
:--- | :---
PRE | Immediately before import processing
POST | Immediately after import processing


### Examples

```xml
<PreImportEvent Description="Pre-Import Event Example" UseInBuild="true">
  <Command>echo Hi! I'm a pre-import command!</Command>
</PreImportEvent>
```

```xml
<PostImportEvent Description="Post-Import Event Example" UseInBuild="true">
  <Command>echo Hi! I'm a post-import command!</Command>
</PostImportEvent>
```


# 1622408596

## New Features

Pyro can read access tokens from a `.secrets` file placed in the program path. This feature allows you to:

- use unique access tokens for each remote,
- store access tokens without revealing them in commands or screenshots, and
- securely store access tokens. _(Disclaimer: The user is responsible for setting the appropriate ownership/permissions.)_

The `.secrets` file is simply an INI file with this familiar format:

```ini
[github.com/fireundubh/LibFire]
access_token = your_personal_access_token
```

The `access_token` option supports user and system environment variables in Python syntax:

```ini
[github.com]
access_token = $ACCESS_TOKEN
```

Each section name is a host URL part that is matched case-insensitively against import URLs.

Host matches occur in sequential order. These host matching rules should be ordered top-down from narrowest to broadest. 

If the `--access-token` argument is passed to Pyro, this argument will take priority over the `.secrets` file regardless of whether the file exists.


## Fixes

- Fixed issue where where `<Script>` paths did not support current and parent directory symbols
- Fixed issue where namespace colon format support could clobber absolute script paths
- Fixed issue where slower built-in endswith and startswith comparators were still in use


# 1622359375

## Fixes

- Fixed issue where compilation did not fail when errors contained negative line or column numbers
- Fixed issue where PermissionError was not logged


# 1618543799

## New Features

A `Path` attribute was added to the `Include` element allowing you to specify where in the `ZipFile` the included file will be located.

```xml
  <ZipFiles Output="@modpath">
    <ZipFile Name="@modname" RootDir="@modpath" Compression="deflate">
      <Include>@modpath\Auto Loot.esp</Include>
      <Include>@modpath\Auto Loot - Main.ba2</Include>
      <Include>@modpath\Non-Playable Flags Patch.esp</Include>
      <Include Path="optional">@modpath\Auto Loot - UFO4P Components Patch.esp</Include>
    </ZipFile>
  </ZipFiles>
```

In the above example, the file `Auto Loot - UFO4P Components Patch.esp` will appear in a top-level folder named `optional` within the ZIP archive.

**Note:** You cannot rename files using this feature. The `Path` attribute is used only to create folders.


# 1617834302

## Changes

- Remote downloads are now parallelized (currently, the number of workers is CPU-bound)
- Project validation now checks compiler and flags paths


## Fixes

- Fixed issue where empty game path produced game type project validation error
- Fixed issue where `Folder` parsing could fail due to unexpected input
- Fixed issue where relative flags path could be returned when path ended with flags file name
- Fixed issue where relative `PapyrusProject.Output` path was not properly converted to absolute path
- Fixed issue where relative `Package.RootDir` path was not properly converted to absolute path

*Thanks to Mr. Octopus (MrNeverLost) for reporting some of these issues!*


# 1613874280

## Hotfix

> An issue was fixed where scripts could not be downloaded from private GitHub remotes.
> 
> *Thanks to Mr. Octopus (MrNeverLost) for reporting the issue!*
{.is-info}


# 1608598199

## New Features

- Added `--no-implicit-imports` argument to disable implicit import discovery


# 1608551127

## Fixes

- Fixed issue where only one compilation error could be logged (originally intended to be helpful but could be confusing)
- Fixed issue where the colon delimiter could not be used in `Folder` paths (e.g., `<Folder>Scripts:Source:User</Folder>`)


# 1603689187

## Hotfix

> An upstream issue with Nuitka 0.6.9.x causes Pyro to hang when executing workers. Each worker is actually crashing with an access violation. Recompiling Pyro through Nuitka 0.6.8.4 circumvents the issue. ([Nuitka Issue 867](https://github.com/Nuitka/Nuitka/issues/867))
> 
> *Thanks to Exit_9B (Parapets) for reporting the issue.*
{.is-info}


## Fixes

- Fixed issue where `--game-type` argument value was not passed forward
- Fixed issue where `--zip-compression` argument was not handled
- Fixed issue where `--game-type` and `--zip-compression` argument values could be not lowercase
- Fixed issue where "game type detected from registry path" warning could print in error
- Fixed issue where "game type detected from registry path" warning could throw KeyError


# 1602008042

## Hotfix

> In Skyrim Special Edition, an issue was recently discovered where packages containing textures can crash the game if they have the Embed File Names flag. To work around this issue, for SSE projects, Pyro will now detect whether packages will contain textures, and if so, pass an argument to BSArch to prevent this flag from being added to the package.
{.is-info}


# 1601138736

## Major Changes

`PreBuildEvent` and `PostBuildEvent` elements have been added to the PyroProject XSD. These parent elements contain `Command` children.


### Options

- A `Description` attribute can be used to clarify each event. This description will be printed in the build output.
- A `UseInBuild` attribute can be used to toggle whether the event is used.


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


## Fixes

- Fixed issue where implicit import paths could be duplicated in merged output
- Fixed issue where Fallout 4 namespaces could not be resolved in some cases
- Fixed issue where Fallout 4 game type could not be determined from registry path
- Fixed issue where excessive whitespace could interfere with build event commands
- Removed JSON-based state logging (TODO: better logging)


# 1597538917

## Fixes

- Fixed issue where implicit import discovery failed quietly when imports were on different drives
- Fixed issue where environment variables were unusable due to character restriction in `<Variable>` element values
- Fixed issue where only some environment variable formats were supported in `<Variable>` element values
- Fixed issue where registry paths could fail to resolve for Fallout games
- Fixed issue where average compilation time dividend was switched around


## Performance

- Increased long path comparison speed with high-efficiency string comparators
- Improved maintainability of PapyrusProject XML Schema Definition (XSD)


# 1589924890

## New Features

Pyro now supports building multiple ZIP archives from a single PPJ. **This is a breaking change.**

- `ZipFile` nodes must descend from the `ZipFiles` node, consistent with other top-level nodes.
- The `Output` attribute was reassigned from the `ZipFile` node to its parent `ZipFiles` node.


### Example

```xml
<ZipFiles Output="@MyProject">
  <ZipFile Name="@ModName - Legendary Edition" RootDir="@MyProject" Compression="deflate">
    <Include>@MyProject\@ModName - Legendary Edition.esp</Include>
    <Include NoRecurse="true">*.bsa</Include>
  </ZipFile>
  <ZipFile Name="@ModName - Special Edition" RootDir="@MyProject" Compression="deflate">
    <Include>@MyProject\@ModName - Special Edition.esp</Include>
    <Include NoRecurse="true">*.bsa</Include>
  </ZipFile>
</ZipFiles>
```

## Fixes

- Fixed issue where node attribute updater failed to run due to obsolete code
- Fixed issue where BSA/BA2 packages created in a session could be clobbered when sharing file name
- Fixed issue where relative `RootDir` path resolution logged failures to wrong logger
- Slightly improved clobber prevention for packages and zip files


# 1589570428

## Fixes

- Fixed issue where Pyro and XSD did not agree on TES5 game type signature
- Updated Python to 3.7.7 
- Updated Nuitka to 0.6.7


# 1579252390

## Fixes

- Fixed issue where anonymizer could fail to run due to bad timestamp comparison
- Fixed issue where anonymizer would log confusing error when targeting anonymized script


# 1579153323

## Major Changes

- Added positional input path argument (usage: `pyro.exe MyProject.ppj`)
- Deprecated optional input path arguments (`-i` and `--input-path` will be phased out)

## Fixes

- Fixed issue where `Output` attribute values could never be `.` even if desired by user
- Fixed issue where `.` was not parsed as project path in `Output` attribute values


# 1578820587

## Major Changes

- Implemented public Bitbucket Cloud remote support (no access token required) *\[Note: This change does not include support for private Bitbucket Cloud repositories or Bitbucket Server repositories.]*

## Fixes

- Fixed issue where failing to load remote URL did not stop download process


# 1578785515

## Fixes

- Fixed issue where files other than scripts were downloaded from remotes
- Fixed issue where local path for folder remote was not also imported


# 1578741974

## Fixes

- Fixed issue where branch refs were not parameterized for converted GitHub API URLs
- Fixed issue where leading and trailing whitespace in PPJ node text could cause unexpected behavior


# 1578739900

## Fixes

- Fixed issue where only master branch remotes were supported


# 1578738572

## Fixes

- Fixed issue where scripts downloaded from remotes for compilation could not be compiled


# 1578730357

## Fixes

- Fixed issue where some remote URLs were not correctly parsed


# 1578728566

## Fixes

- Fixed issue where libraries needed for remote support were missing
- Fixed issue where recursively importing from remotes yielded unexpected compilation results (now only the local path first created for the remote URL will be added to Includes and Folders)
- Fixed issue where casing could prevent resolution of remote URLs


# 1578640616

## Major Changes

### Dumping PEX headers

When a PEX file is passed to Pyro, Pyro will dump the header to stdout.
```
Usage: pyro -i file.pex
```

### Dumping PPJ files with resolved paths

When a PPJ file is passed to Pyro and the `--resolve-ppj` argument is provided, Pyro will resolve any variables and dump the contents to stdout.
```
Usage: pyro -i myproject.ppj --resolve-ppj
```

### Using remote imports

When a GitHub URL is used as an `Import` path, Pyro will download the respective files and use the download location as the import path.
```xml
<Import>https://github.com/fireundubh/skyui/tree/master/dist/Data/Scripts/Source</Import>
<Import>https://api.github.com/repos/fireundubh/skyui/contents/dist/Data/Scripts/Source?ref=master</Import>
```

To import from GitHub repositories, the following arguments have been added:

Argument | Required | Type | Description | Default Value
:--- | :--- | :--- | :--- | :---
`--access-token` | `true` (when using remotes) | `bool` | [your personal access token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line)<br>(must have `public_repo` access scope) | 
`--force-overwrite` | `false` | `bool` | download remote files and overwrite existing files<br>(default: skip download when remote folder exists) | `false`
`--remote-temp-path` | `false` | `str` | relative or absolute path to temp folder for remote files<br>(if relative, must be relative to project) | `{program_path}\remote`

## Enhancements

- Limited priority of parallel processes to "below normal"
- Implemented anonymization of script paths in compiled script headers
- Added compilation statistics to build output (e.g., # of scripts, # of successes, # of failures, time per script, total time)
- Allowed using current directory symbol as `RootDir` path in `Include` nodes
- Allowed using absolute folder paths within `RootDir` in `Include` nodes
- Allowed using environment and user variables in PPJ files
- Under-the-hood optimizations and reduced overall memory footprint

## Fixes

- Fixed issue where glob expressions could be parsed incorrectly
- Fixed issue where compiled scripts were not packaged when deeper `RootDir` passed (e.g., `@project\scripts`)
- Fixed issue where files outside `RootDir` could be zipped
- Fixed issue where excessively long commands (>32768 chars) could be passed to the compiler
- Fixed issue where time values were subject to floating point errors
- Fixed issue where TimeElapsed values were not converted from floats to Decimal
- Fixed issue where ZeroDivisionError could be raised when computing average compilation time
- Fixed issue where build process would continue if scripts failed to compiled
- Fixed issue where packaging failed late if existing packages could not be overwritten
- Fixed issue where duplicate package names were not properly changed
- Fixed issue where scripts that import other scripts would fail to compile if imported scripts were not first compiled
- Fixed issue where unnecessary import paths were passed to compiler which could produce strange errors
- Updated Nuitka to 0.6.6


# 1575000759

## Fixes

- Fixed issue where variable substitutions in `Variable` values were executed in only first-last order


# 1574827307

## Fixes

- Further restricted `Variable` names to only alphanumeric characters


# 1574826016

## Major Changes

Pyro now allows `Variable` values to reference themselves and other variables. For example:

```xml
<Variables>
	<Variable Name="modname" Value="Auto Loot"/>
	<Variable Name="modpath" Value="E:\ModOrganizer\Games\Fallout4\mods\@modname"/>
</Variables>
```

In addition, the following characters are reserved and cannot be used in `Variable` names or values:
```
!    #    $    %    ^    &    *
```
Whitespace, such as spaces and tabs, cannot be used in `Variable` names. The `@` character is also reserved but can be used in `Variable` values.


## Fixes

- Fixed issue where whitespace and reserved characters could be used in variable names
- Fixed issue where reserved characters could be used in variable values


# 1574772562

## Fixes

- Fixed issue where globbing files from `Folder` paths collected paths to all types of files
- Fixed issue where compiler could be sent duplicate commands
- Optimized process runner for when either no scripts or only one script would be compiled


# 1574759796

## Major Changes

- Pyro can create multiple BSA/BA2 packages if they are defined in the PPJ.
- Pyro can create a ZIP archive containing specific files if they are defined in the PPJ.
- Pyro can expand variables in paths and string-type attributes if they are defined in the PPJ.
- The `Archive` attribute of the `PapyrusProject` node was removed.
- The `--anonymize` and `--bsarch` arguments were removed.


### Packaging

Pyro can now create multiple packages using the `Packages` node block.
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
**Note:** Glob patterns are limited to "match everything" expressions, such as `*.pex` and `**\*.psc`. 

#### Default Values

Node | Attribute | Default Value | Required
:--- | :--- | :--- | :---
`Packages` | `Output` | Path to `pyro/dist` folder | No
`Package` | `Name` | If the attribute is omitted:<br>- the package file will be named after the project,<br>- the extension will be appropriate to the game, and<br>- subsequent package names will be suffixed with `(1)`, `(2)`, and so on.  | No
`Package` | `RootDir` | Path to the project folder | Yes
`Include` | `NoRecurse` | false | No

### Zipping

Pyro can now create a ZIP archive containing specific files using the `ZipFile` node block.
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
**Note:** Glob patterns are limited to "match everything" expressions, such as `*.pex` and `**\*.psc`.

#### Default Values

Node | Attribute | Default Value | Required
:--- | :--- | :--- | :---
`ZipFile` | `Name` | If the attribute is omitted, the ZIP file will be named after the project. | No
`ZipFile` | `RootDir` | Path to the project folder | Yes
`ZipFile` | `Output` | Path to `pyro/dist` folder | No
`ZipFile` | `Compression` | deflate | No
`Include` | `NoRecurse` | false | No

### Variables

Pyro can substitute variables with defined values in PPJ paths and string attributes.
```xml
<Variables>
  <Variable Name="namespace" Value="Master of Disguise"/>
  <Variable Name="modname" Value="Master of Disguise - Special Edition"/>
  <Variable Name="myproject" Value="E:\projects\skyrim\Master of Disguise - Special Edition"/>
</Variables>
```
Variables are prefixed with the `@` symbol. The `Name` and `Value` attributes are required.
```xml
<ZipFile Name="@modname" RootDir="@myproject" Output="@myproject" Compression="deflate">
  <Include>@myproject\@modname.esp</Include>
  <Include NoRecurse="true">*.bsa</Include>
</ZipFile>
```

### New PapyrusProject Attributes

The `Package` and `Zip` boolean attributes have been added to allow enabling and disabling packaging and zipping.
```xml
<PapyrusProject
  xmlns="PapyrusProject.xsd"
  Flags="TESV_Papyrus_Flags.flg"
  Output="@myproject\scripts"
  Optimize="true" Anonymize="true" Package="true" Zip="true">
```

#### Default Values

Node | Attribute | Default Value | Required
:--- | :--- | :--- | :---
`PapyrusProject` | `Package` | false | No
`PapyrusProject` | `Zip` | false  | No


## Fixes

- Fixed issue where schema validation could fail on the `Asm` attribute due to case sensitivity
- Fixed issue where absolute `Include` paths were not constrained to the `RootDir` directory


# 1574589710

## Major Changes

- By default, Pyro will no longer anonymize compiled scripts. The `--anonymize` argument must be used or the `Anonymize` attribute must be set to `true`.
- By default, Pyro will no longer automatically create BSA/BA2 packages. The `--bsarch` argument must be used or the `CreateArchive` attribute must be set to `true`.
- Consequently, the `--no-anonymize` and `--no-bsarch` arguments were removed.

## Fixes

- Improved and optimized missing compiled scripts discovery
- Fixed issue where the order of operations executed during PapyrusProject initialized produced unexpected behavior
- Fixed issue where a previous improvement to pre-build compiled scripts discovery returned only paths to existing files


# 1574552852

## Major Changes

- When the game type is not explicitly defined, Pyro will also attempt to discover the game type using the `--registry-path` argument.
- When using XSD validation, Pyro will terminate if the `Game` attribute value does not contain a valid game type.

## Fixes

- Fixed issue where some paths were not normalized
- Fixed issue where some input path validation tests were case sensitive
- Fixed issue where input paths prefixed with `file:/` or `file://` were not parsed correctly
- Fixed issue where logging deprecation warnings were output to console


# 1574531277

## Major Changes

- When using XSD validation, Pyro allows the Imports, Folders, Scripts, and Includes nodes to appear in any order. This is a further improvement by Pyro on how Papyrus Projects are handled by the Papyrus Compiler for Fallout 4 which enforces a specific order.
- When the game type is not explicitly defined, Pyro attempts to discover the game type first using arguments then the game path, import paths, and finally the flags path. The game type will generally be discoverable from imports; nearly every project imports base game scripts. For Skyrim projects, the game type is less accurately discoverable from the flags path because the flags file for SSE and TESV share the same name. If Pyro uses this last resort, the game type will default to SSE if the game *path* for SSE can be discovered as well.

## Fixes

- Fixed issue where passing the full registry path with `--registry-path` was not handled correctly


# 1574491427

## Major Changes

- If the `xmlns` attribute of the PapyrusProject node is set to a valid XML Schema path, Pyro will use that XSD file to validate the PPJ.
- The `NoRecurse` attribute was removed from the `Folders` node. Each `Folder` node now has an independent `NoRecurse` attribute.
- `Include` nodes now support relative folder paths. Each `Include` node now has an independent `NoRecurse` attribute.
- Comments, including XML-unsupported comments, can now be used in PPJs.

### XML Schema Validation

```xml
<PapyrusProject xmlns="PapyrusProject.xsd">
```

Pyro will look for the file named `PapyrusProject.xsd` in the program path. If this attribute is omitted, Pyro will not validate the PPJ.

### Folder Recursion

```xml
  <Folders>
    <Folder NoRecurse="true">Master of Disguise</Folder>
  </Folders>
```

When `NoRecurse` is enabled, Pyro will not compile scripts in subfolders within the given folder. By default, `NoRecurse` is disabled.

### Include Folders

```xml
  <Includes Root="E:\projects\skyrim\Master of Disguise - Special Edition">
    <Include NoRecurse="false">interface</Include>
  </Includes>
```

When `NoRecurse` is disabled, Pyro will recursively add files in this folder and its subfolders to the output BSA/BA2. By default, `NoRecurse` is disabled.

### Comments Allowed

```xml
<PapyrusProject
<!--  xmlns="PapyrusProject.xsd" -->
  Game="sse"
  Flags="<!-- TESV_Papyrus_Flags.flg -->"
  Output="E:\projects\skyrim\Master of Disguise - Special Edition\scripts"
  Archive="E:\projects\skyrim\Master of Disguise - Special Edition\Master of Disguise - Special Edition.bsa"
  Optimize="true">
```

These are not valid XML comments because they appear within element tags and attribute values. XML-unsupported comments will cause validators and syntax highlighters to treat the PPJ as malformed. Pyro will strip all supported and unsupported comments virtually before parsing the PPJ to avoid parsing errors.

## Fixes

- Fixed issue where passing an invalid input path (e.g., a nonexistent PPJ file) would produce an unhandled exception
- Fixed issue where deeply nested Fallout 4 script paths were not resolved correctly (e.g., `AutoLoot\Fragments\Terminals\TERM_AutoLoot_312_04001137.psc`)
- Fixed issue where Fallout 4 scripts were compiled repeatedly


# 1574388420

## Major Changes

- Improving compatibility with other tools, Pyro can be configured with CLI arguments instead of INI settings. In addition, users can use the `--worker-limit` argument to fine tune the maximum number of compiler processes spawned.
- All PPJ attributes are optional. If PPJ attributes are not configured, Pyro will use default values.
- Pyro uses an incremental build system that compares timestamps embedded in compiled scripts with the last modified timestamps on source scripts, instead of recording and comparing hashes in an external file.
- Path handling has been significantly improved to achieve parity with the Fallout 4 Papyrus Compiler CLI. Pyro will check if paths are absolute, if they're relative to the input PPJ, and if they're relative to Imports. Only the first valid match will be used.
- Implicit import path discovery has been significantly improved. Pyro will evalute paths in Folders and Scripts to use any relevant paths missing from the Imports declaration.


## Fixes

- Allowed `xmlns` attribute to be optional
- Fixed issue where `CreateArchive` and `Anonymize` default values were always used
- Fixed issue where `Release`, `Final`, and `Optimize` values were not properly checked for 'true' or '1'
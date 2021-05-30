---
title: Contributing
description: 
published: true
date: 2021-05-30T23:22:52.263Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:22:52.263Z
---

# Compiling

1. Install [PyCharm Community Edition](https://www.jetbrains.com/pycharm/download/).
2. Clone the `dev` repository from GitHub.
3. Using PyCharm, open the folder where that repo was cloned.
4. Using PyCharm, create a virtual environment with `virtualenv`.
5. Using PyCharm, install the requirements from `requirements.txt`.
6. To compile, using PyCharm, create a new Run/Debug Configuration (as shown below) and run that configuration:

![Build Nuitka Binaries](https://i.imgur.com/y7tBXp0.jpg)

> **Note:** The build process requires [Nuitka](https://nuitka.net/)  and the [Visual Studio](https://visualstudio.microsoft.com/downloads/) build tools. Nuitka was installed in the previous step. Executing the build script will create a `pyro.dist` directory that contains the executable and required libraries and modules. A ZIP archive will be created in the `bin` folder.
{.is-info}



## Optional Build Script Arguments

The build script has three arguments.

Short Argument | Long Argument |  Help
:--- | :--- | :---
&mdash; | `--no-zip` | Skips ZIP generation. Useful for CI.
&mdash; | `--vcvars64-path` | Path to Visual Studio Developer Command Prompt (x64)


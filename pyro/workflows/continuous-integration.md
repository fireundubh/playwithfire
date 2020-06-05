---
title: Continuous Integration
description: 
published: true
date: 2020-06-05T10:23:28.482Z
tags: 
---

# Overview

This workflow is entirely theoretical and has not been tested.

# Requirements

ID | Requirement | Notes
:--- | :--- | :--- 
`VirtualMachine` | Windows Server 2019 | `PapyrusCompiler.exe` is a .NET application and requires a window, so `wine` or `mono` on a Linux server would have trouble running this process.
`FileServer` | HTTPS or SFTP Server | The `Papyrus Compiler` and the `Data\Scripts\Source` folders and their contents would need to be hosted on a file server. They can be hosted in ZIP files and later extracted by the build script.<br><br>Ideally, Bethesda Softworks would create GitHub repositories for these files; otherwise, the file server should be secured so as to avoid publicly distributing Bethesda's assets.<br><br>In addition, to protect server credentials, the project's repo would need to be private.

# Workflow Diagram 

```mermaid
stateDiagram
  [*] --> GitHub
	GitHub --> PullRequest
	PullRequest --> CodeReview
	CodeReview --> PullRequest
	CodeReview --> Actions
  Actions --> VirtualMachine
  FileServer --> VirtualMachine
  Python --> VirtualMachine
  VirtualMachine --> PapyrusProject
  PapyrusProject --> Pyro
	Pyro --> PapyrusCompiler
  PapyrusCompiler --> PapyrusAssembler
  Pyro --> BSArch
  PapyrusAssembler --> zipfile
  BSArch --> zipfile
  zipfile --> Artifacts
  Artifacts --> Testing
  Testing --> [*]
  Artifacts --> Releases
  Artifacts --> NexusMods
```
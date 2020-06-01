---
title: Pyro Workflows
description: 
published: true
date: 2020-06-01T11:45:01.096Z
tags: 
---

# GitHub Actions

## Requirements

ID | Requirement | Notes
:--- | :--- | :--- 
`VirtualMachine` | Windows Server 2019 | `PapyrusCompiler.exe` is a .NET application and requires a window, so `wine` or `mono` on a Linux server would have trouble running this process.
`FileServer` | HTTPS or SFTP Server | The `Papyrus Compiler` and the `Data\Scripts\Source` folders and their contents would need to be hosted on a file server. They can be zipped and extracted by the build script.<br><br>Ideally, Bethesda Softworks would create GitHub repositories for these files; otherwise, the file server should be secured so as to avoid publicly distributing Bethesda's assets.<br><br>In addition, to protect the file server credentials, the project's GitHub repo would need to be private.

## Workflow Diagram 

```mermaid
stateDiagram
	GitHub --> PullRequest
	PullRequest --> CodeReview
	CodeReview --> PullRequest
	CodeReview --> Actions
  Actions --> VirtualMachine
  FileServer --> VirtualMachine
  VirtualMachine --> Pyro
	Pyro --> PapyrusCompiler
  PapyrusCompiler --> PapyrusAssembler
  Pyro --> BSArch
  PapyrusAssembler --> zipfile
  BSArch --> zipfile
  zipfile --> Artifacts
```
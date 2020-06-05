---
title: Continuous Integration with Test Automation
description: 
published: true
date: 2020-06-05T10:39:06.360Z
tags: 
---

# Overview

This workflow is not possible given the available tools today.

# Requirements

ID | Requirement | Notes
:--- | :--- | :--- 
`PapyrusLinter` | Linter | A lexer/parser for Papyrus would allow Pyro to offer code analysis, syntax checking, code clone cleanup, and refactoring assistance. Alternatively, the Papyrus Compiler can be patched to output the AST, and Pyro can use that AST directly.
`TestRunner` | Plugin verification test runner | An xEdit-based CLI would enable Pyro to verify that paths to BSA/BA2 assets in records are correct, verify that script properties are filled and used, and execute other user-defined verification tests.

# Workflow Diagram 

```mermaid
stateDiagram
  [*] --> GitHub
	GitHub --> PullRequest
	PullRequest --> CodeReview
	CodeReview --> PullRequest
	CodeReview --> Actions: PR Approved
  Actions --> VirtualMachine
  FileServer --> VirtualMachine
  Python --> VirtualMachine
  VirtualMachine --> PapyrusProject
  PapyrusProject --> Pyro
  Pyro --> PapyrusLinter
  PapyrusLinter --> [*]: Tests Failed
	PapyrusLinter --> PapyrusCompiler: Tests Passed
  PapyrusCompiler --> PapyrusAssembler
  Pyro --> BSArch
  PapyrusAssembler --> zipfile
  BSArch --> zipfile
  zipfile --> Artifacts
  Artifacts --> TestRunner
  TestRunner --> Releases: Tests Passed
  TestRunner --> Testing: Tests Failed
  Testing --> [*]
  Releases --> NexusMods: Release Approved
```
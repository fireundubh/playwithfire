---
title: Action Validation Requirements
description: 
published: true
date: 2022-04-25T08:13:54.467Z
tags: 
editor: markdown
dateCreated: 2022-04-24T07:40:47.909Z
---

# Packages

## create-package

Argument | Value | Validation?
:--- | :--- | ---:
`SourcePath` | existing directory path | `true`
`DestinationPath` | target file path | `false`

## extract-package

Argument | Value | Validation?
:--- | :--- | ---:
`SourcePath` | existing file path | `true`
`DestinationPath` | target directory path | `false`

## extract-single-file

Argument | Value | Validation?
:--- | :--- | ---:
`SourcePath` | existing file path | `true`
`DestinationPath` | target file path | `false`

## list-package

Argument | Value | Validation?
:--- | :--- | ---:
`SourcePath` | existing file path | `true`


# Conversion

## convert-model

Argument | Value | Validation?
:--- | :--- | ---:
`SourcePath` | existing file path | `true`
`DestinationPath` | target file path | `false`

## convert-resource

Argument | Value | Validation?
:--- | :--- | ---:
`SourcePath` | existing file path | `true`
`DestinationPath` | target file path | `false`


# Batch

## extract-packages

Argument | Value | Validation?
:--- | :--- | ---:
`SourcePath` | existing directory path, contains packages | `true`
`DestinationPath` | target directory path | `false`

## convert-models

Argument | Value | Validation?
:--- | :--- | ---:
`SourcePath` | existing directory path, contains models | `true`
`DestinationPath` | target directory path | `false`

## convert-resources

Argument | Value | Validation?
:--- | :--- | ---:
`SourcePath` | existing directory path, contains packages | `true`
`DestinationPath` | target directory path | `false`

---
title: Import Events
description: 
published: true
date: 2021-05-31T19:35:47.749Z
tags: 
editor: markdown
dateCreated: 2021-05-31T19:35:47.749Z
---

**Import Events** are sequences of shell commands that execute before and after imports are processed.

Pyro supports pre-import events and post-import events.


# Options

The `PreImportEvent` and `PostImportEvent` elements have the following attributes:

- A `Description` attribute can be used to clarify each event to the user. This description will also be logged in the build output.
- A `UseInBuild` attribute can be used to toggle whether the event is used.

The `Command` element does not have any attributes.


# Timing

Event | Runs When
:--- | :---
PRE | Immediately before import processing
POST | Immediately after import processing


# Examples

```xml
<PreImportEvent Description="Pre-Import Event Example" UseInBuild="true">
  <Command>echo Hi! I'm a pre-import command!</Command>
</PreImportEvent>
```

```xml
<PostImportEvent Description="Post-Import Event Example" UseInBuild="true">
  <Command>echo Hi! I'm a post-import command!</Command>
</PostImportEvent >
```

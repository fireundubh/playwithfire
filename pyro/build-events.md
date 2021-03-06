---
title: Build Events
description: 
published: true
date: 2021-05-31T19:36:37.660Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:19:39.288Z
---

**Build Events** are sequences of shell commands that execute before and after the project builds.

Pyro supports pre-build events and post-build events.


# Options

The `PreBuildEvent` and `PostBuildEvent` elements have the following attributes:

- A `Description` attribute can be used to clarify each event to the user. This description will also be logged in the build output.
- A `UseInBuild` attribute can be used to toggle whether the event is used.

The `Command` element does not have any attributes.


# Timing

Event | Runs When
:--- | :---
PRE | Immediately before compilation
POST | Immediately after build success


# Examples

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


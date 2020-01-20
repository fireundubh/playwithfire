---
title: Not removing unused code
description: 
published: true
date: 2020-01-20T12:16:15.566Z
tags: 
---

# Anti-pattern

Changing scripts in fundamental ways may result in code, such as functions and properties, becoming obsolete, and that unused code may not be cleaned up.

Alternatively, a developer may have intended to save old code in the event they want to refer back to that code.

# Best practice

Find and remove unused code to keep script sources clean, focused, and relevant. For archival purposes, store old code elsewhere.

Removing unused code will reduce script sizes, and when unused properties are removed, Papyrus will not log unused property warnings.
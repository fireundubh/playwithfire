---
title: Remotes
description: 
published: true
date: 2021-05-31T11:00:58.163Z
tags: 
editor: markdown
dateCreated: 2021-05-30T23:17:03.187Z
---


Pyro can import and download scripts from GitHub and public Bitbucket Cloud repositories.

# Importing scripts

When a GitHub or public Bitbucket Cloud URL is used as an `Import` path, Pyro will download the respective files and use the download location as the import path.

For example:

```xml
<Imports>
  <!-- Pyro will accept a GitHub page address. -->
  <Import>https://github.com/fireundubh/skyui/tree/master/dist/Data/Scripts/Source</Import>
  <!-- Pyro will also accept a GitHub API address. -->
  <Import>https://api.github.com/repos/fireundubh/skyui/contents/dist/Data/Scripts/Source?ref=master</Import>
</Imports>
```

# Compiling scripts

When a GitHub or public Bitbucket Cloud URL is used as an `Folder` path, Pyro will download the respective files and use the download location as the folder path.

For example:

```xml
<Folders>
  <!-- Pyro will accept a GitHub page address. -->
  <Folder NoRecurse="false">https://github.com/chesko256/Campfire/tree/master_fo4/Scripts/Source</Folder>
  <!-- Pyro will also accept a GitHub API address. -->
  <Folder NoRecurse="false">https://api.github.com/repos/chesko256/Campfire/contents/Scripts/Source?ref=master_fo4</Folder>
</Folders>
```

If the `NoRecurse` attribute is set to `true`, all remote files will still be downloaded but only scripts in the initial folder will be compiled.


# Access tokens

GitHub repositories require a [personal access token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line). Your token must have `public_repo` access scope.

You can specify a global access token for all repositories in your project file using the `--access-token` argument, or you can create a `.secrets` file in the program path defining unique access tokens for each repository.

Public Bitbucket Cloud repositories do not require an access token.

## Secrets File

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

If the `--access-token` argument is provided, the value will take priority over the `.secrets` file regardless of whether the file exists.


# CLI Arguments

## --access-token

- **description:** your personal access token (must have `public_repo` access scope)
- **default value:** `''`
- **argument type:** `str`

## --force-overwrite

- **description:** download remote files and overwrite existing files
- **default value:** `false`
- **argument type:** `bool`

## --remote-temp-path

relative or absolute path to temp folder for remote files (if relative, must be relative to project)

- **description:** relative or absolute path to temp folder for remote files (if relative, must be relative to project)
- **default value:** `{program_path}\remote`
- **argument type:** `str`

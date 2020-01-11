<!-- TITLE: Papyrus Project Schema -->

# Papyrus Project Schema
## Attribute Defaults

### PapyrusProject

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`PapyrusProject` | `Game` | `str` | (determined programmatically)
`PapyrusProject` | `Output` | `str` | Path to the `pyro\out` folder
`PapyrusProject` | `Flags` | `str` | (determined programmatically from game path)
`PapyrusProject` | `Optimize` | `bool` | `false`
`PapyrusProject` | `Release` (FO4 only) | `bool` | `false`
`PapyrusProject` | `Final` (FO4 only) | `bool` | `false`
`PapyrusProject` | `Anonymize` | `bool` | `false`
`PapyrusProject` | `Package` | `bool` | `false`


### Folder

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Folder` | `NoRecurse` | `bool` | `false`


### Packages

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Packages` | `Output` | `str` | Path to the `pyro\dist` folder
`Package` | `Name` | `str` | If the attribute is omitted:<ul><li>the package file will be named after the project,<li>the extension will be appropriate to the game, and<li>subsequent package names will be suffixed with `(1)`, `(2)`, and so on.</ul>
`Package` | `RootDir` | `str` | Path to the project folder 
`Include` | `NoRecurse`  | `bool` | `false`


### ZipFile

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`ZipFile` | `Name` | `str` | If the attribute is omitted, the ZIP file will be named after the project.
`ZipFile` | `RootDir` | `str` | Path to the project folder
`ZipFile` | `Output` | `str` | Path to the `pyro\dist` folder
`ZipFile` | `Compression` | `str` | `deflate`
`Include` | `NoRecurse` | `bool` | `false`
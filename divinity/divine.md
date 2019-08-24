<!-- TITLE: Divine CLI -->

# Divine CLI
## Usage

### Required Arguments

Required | Short | Long | Allowed Values | Description
:--- | :--- | :--- | :--- | :---
`True` | `-s` | `--source` | must be an absolute file/folder path | Set source file path or directory
`True` | `-a` | `--action` | <ul><li>`create-package`<li>`list-package`<li>`extract-single-file`<li>`extract-package` (default)<li>`extract-packages`<li>`convert-model`<li>`convert-models`<li>`convert-resource`<li>`convert-resources`</ul> | Set action to execute

### Optional Arguments

Required | Short | Long | Allowed Values | Description
:--- | :--- | :--- | :--- | :---
`False` | `-l` | `--loglevel` | <ul><li>`off`<li>`fatal`<li>`error`<li>`warn`<li>`info` (default)<li>`debug`<li>`trace`<li>`all`</ul> | Set verbosity level of log output
`False` | `-g` | `--game` | <ul><li>`dos`<li>`dosee`<li>`dos2` (default)<li>`dos2de`</ul> | Set target game when generating output
`False` | `-d` | `--destination` | must be an absolute file/folder path | Set destination file path or directory
`False` | `-f` | `--packaged-path` | | File to extract from package
`False` | `-i` | `--input-format` | | Set input format for batch operations
`False` | `-o` | `--output-format` | | Set output format for batch operations
`False` | `-p` | `--package-version` | | Set package version
`False` | `-c` | `--compression-method` | | Set compression method
`False` | `-e` | `--gr2-options` | | Set extra options for GR2/DAE conversion
`False` | `-x` | `--expression` | | Set glob expression for extract and list actions

### Switch Arguments

Required | Long | Description
:--- | :--- | :--- | :---
`False` | `--conform-path` | Set conform to original path
`False` | `--use-package-name` | Use package name for destination folder
`False` | `--use-regex` | Use Regular Expressions for expression type
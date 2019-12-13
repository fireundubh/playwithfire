<!-- TITLE: Not removing unused code -->

# Not removing unused code
## Anti-pattern

Changing scripts in fundamental ways may result in code, such as functions and properties, becoming obsolete, and that unused code may not be cleaned up.

Alternatively, a developer may have intended to save old code in the event they want to refer back to that code.

## Best practice

Find and remove unused code to keep script sources clean, focused, and relevant. For archival purposes, store old code elsewhere.

Removing unused code will reduce script sizes, and when unused properties are removed, Papyrus will not log unused property warnings.
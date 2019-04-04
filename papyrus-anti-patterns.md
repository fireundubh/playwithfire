<!-- TITLE: Papyrus Anti-Patterns -->

# Papyrus Anti-Patterns

> "An **anti-pattern** is like a pattern, except that instead of a solution it gives something that looks superficially like a solution, but isn't one." —Andrew Koenig, who originally coined the term in 1995

This working document aims to present all the ways modders write "bad Papyrus" and how to avoid doing so. It is modeled after [The Little Book of Python Anti-Patterns](https://docs.quantifiedcode.com/python-anti-patterns/index.html).

## Correctness

- [Not returning a value on all code paths](papyrus-anti-patterns/not-returning-a-value-on-all-code-paths)
- [Not using a break condition in a loop](papyrus-anti-patterns/not-using-a-break-condition-in-a-loop)
- [Not validating arrays before accessing array elements](papyrus-anti-patterns/not-validating-arrays-before-accessing-array-elements)
- [Not validating objects or arguments before calling a function](papyrus-anti-patterns/not-validating-objects-or-arguments-before-calling-functions)
- [Not validating the length of a dynamic array](papyrus-anti-patterns/not-validating-the-length-of-a-dynamic-array)
- [Passing a zero denominator to a division or modulus operation](papyrus-anti-patterns/passing-a-zero-denominator-to-a-division-or-modulus-operation)

## Maintainability

- [Not removing orphaned functions](papyrus-anti-patterns/not-removing-orphaned-functions) (no page yet)
- [Not removing orphaned properties](papyrus-anti-patterns/not-removing-orphaned-properties) (no page yet)
- [Using a compound conditional statement instead of logic gates](papyrus-anti-patterns/using-a-compound-conditional-statement-instead-of-logic-gates)
- [Using a single letter to name your variables](papyrus-anti-patterns/using-a-single-letter-to-name-your-variables)
- [Using a variable to store a property value used once](papyrus-anti-patterns/using-a-variable-to-store-a-property-value-used-once)
- [Using multiple code paths in boolean functions](papyrus-anti-patterns/using-multiple-code-paths-in-boolean-functions)

## Readability

- [Indentation contains mixed spaces and tabs](papyrus-anti-patterns/indentation-contains-mixed-spaces-and-tabs) (no page yet)
- [Indentation contains spaces](papyrus-anti-patterns/indentation-contains-spaces) (no page yet)

## Performance

- [Using nested loops](papyrus-anti-patterns/using-nested-loops)
- [Passing the player reference to the Activate function](papyrus-anti-patterns/passing-the-player-reference-to-the-activate-function)

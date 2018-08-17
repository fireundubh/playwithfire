<!-- TITLE: Papyrus Anti-Patterns -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Papyrus Anti-Patterns

> "An **anti-pattern** is like a pattern, except that instead of a solution it gives something that looks superficially like a solution, but isn't one." —Andrew Koenig, who originally coined the term in 1995

This working document aims to present all the ways modders write "bad Papyrus" and how to avoid doing so. It is modeled after [The Little Book of Python Anti-Patterns](https://docs.quantifiedcode.com/python-anti-patterns/index.html).

## Correctness

- [Not returning a value on all code paths](not returning a value on all code paths)
- [Not using a break condition in a loop](not using a break condition in a while loop)

## Maintainability

- [Using a single letter to name your variables](using a single letter to name your variables)
- [Using a variable to store a property value used once](using a variable to store a property value used once)

## Readability

- [Indentation contains mixed spaces and tabs](indentation contains mixed spaces and tabs)
- [Indentation contains spaces](indentation contains spaces)

## Performance

- [Using nested loops](using nested while loops)


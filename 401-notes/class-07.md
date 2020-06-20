# Scope

>`scope` rules how variables and names are looked up in your code. It determines the visibility of a variable within the code.

LEGB rule
---
- Local - The names that you define in this scope are only available or visible to the code within the scope.
- Enclosing - is a special scope that only exists for nested functions.
- Global - The names that you define in this scope are available to all your code.
- Built-in - is a special Python scope that’s created or loaded whenever you run a script or open an interactive session.

>  Python scopes are implemented as dictionaries that map names to objects

> Names that you define in the enclosing Python scope are commonly known as nonlocal names

From the moment you start a Python program, you’re in the global Python scope

- You can’t modify names in the enclosing scope from inside a nested function unless you declare them as nonlocal in the nested function


[Main Page](https://will-ing.github.io/reading-notes)
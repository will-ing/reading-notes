# Classes and Objects

`Objects` are an encapsulation of variables and functions into a single entity.

`Classes` are essentially a template to create your objects.

> To access a function inside of an object you use notation similar to accessing a variable:

```py
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

objects = MyClass()

objects.variable
```



---
## Recursive Functions

> The typical structure of a recursive algorithm is that the current problem represents a simple case, solve it. If not, divide it into subproblems and apply the same strategy to them.

A `recursive` function is a function defined in terms of itself via self-referential expressions.

Recursive function for calculating n! implemented in Python:

```py
def factorial_recursive(n):
    # Base case: 1! = 1
    if n == 1:
        return 1

    # Recursive case: n! = n * (n-1)!
    else:
        return n * factorial_recursive(n-1)
```

Each recursive call has its own execution content.

How to maintain state in a recursive call -

- Thread the state through each recursive call so that the current state is part of the current call’s execution context
- Keep the state in global scope

```py
def sum_recursive(current_number, accumulated_sum):
    # Base case
    # Return the final state
    if current_number == 11:
        return accumulated_sum

    # Recursive case
    # Thread the state through the recursive call
    else:
        return sum_recursive(current_number + 1, accumulated_sum + current_number)
```
> A data structure is recursive if it can be deﬁned in terms of a smaller version of itself.

Using recursion in the nth Fibonacci number:

```py
def fibonacci_recursive(n):
    print("Calculating F", "(", n, ")", sep="", end=", ")

    # Base case
    if n == 0:
        return 0
    elif n == 1:
        return 1

    # Recursive case
    else:
        return fibonacci_recursive(n-1) + fibonacci_recursive(n-2)
```

---
## Pytesting

`Fixtures` - objects that might contain data you want to share across tests, or they might involve the network or filesystem

- You can decide how often a fixture is run
- You can mention it in the test's parameter list. Then, inside the test, you can access the fixture by name
- To test a fixture you'll need to pass it a file-like object
- If your fixture uses "yield" instead of "return", pytest understands that the post-yield code is for tearing down objects and connections.

More on fixture:

- fixtures have explicit names and are activated by declaring their use from test functions, modules, classes or whole projects.
- fixtures are implemented in a modular manner, as each fixture name triggers a fixture function which can itself use other fixtures.
- fixture management scales from simple unit to complex functional testing, allowing to parametrize fixtures and tests according to configuration and component options, or to re-use fixtures across function, class, module or whole test session scopes.

Pytest has built-in fixture:

Name | Description
--- | ---
capfd | Capture, as text, output to file descriptors 1 and 2.
capfdbinary | Capture, as bytes, output to file descriptors 1 and 2.
caplog | Control logging and access log entries.
capsys | Capture, as text, output to sys.stdout and sys.stderr.
capsysbinary | Capture, as bytes, output to sys.stdout and sys.stderr.
cache | Store and retrieve values across pytest runs.
doctest_namespace | Provide a dict injected into the docstests namespace.
monkeypatch  | Temporarily modify classes, functions, dictionaries, os.environ, and other objects.
pytestconfig | Access to configuration values, pluginmanager and plugin hooks.
record_property | Add extra properties to the test.
record_testsuite_property | Add extra properties to the test suite.
recwarn | Record warnings emitted by test functions.
request | Provide information on the executing test function.
testdir | Provide a temporary test directory to aid in running, and testing, pytest plugins.
tmp_path | Provide a pathlib.Path object to a temporary directory which is unique to each test function.
tmp_path_factory | Make session-scoped temporary directories and return pathlib.Path objects.
tmpdir | Provide a py.path.local object to a temporary directory which is unique to each test function; replaced by tmp_path.
tmpdir_factory | Make session-scoped temporary directories and return py.path.local objects; replaced by tmp_path_factory.

[Main Page](https://will-ing.github.io/reading-notes)
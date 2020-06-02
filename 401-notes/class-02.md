
# Modules and packages 

`Modular programming` refers to the process of breaking a large, unwieldy programming task into separate, smaller, more manageable subtasks or modules.

Advantages
* Simplicity
* Maintainability
* Reusability
* Scoping

3 ways to define a `module` in `Python`
1. A module can be written in Python itself.
1. A module can be written in C and loaded dynamically at run-time, like the re (regular expression) module.
1. A built-in module is intrinsically contained in the interpreter, like the itertools module.

```py
import sys
sys.path
['', 'C:\\Users\\john\\Documents\\Python\\doc', 'C:\\Python36\\Lib\\idlelib',
'C:\\Python36\\python36.zip', 'C:\\Python36\\DLLs', 'C:\\Python36\\lib',
'C:\\Python36', 'C:\\Python36\\lib\\site-packages']
```

> Module contents are made available to the caller with the import statement. The import statement takes many different forms, shown below.

# Pytest 

> The `pytest` framework makes it easy to write small tests, yet scales to support complex functional testing for applications and libraries.

pytest example

```py
# content of test_sample.py
def inc(x):
    return x + 1


def test_answer():
    assert inc(3) == 5
```

why use pytest?

* Very easy to start with because of its simple and easy syntax.
* Can run tests in parallel.
* Can run a specific test or a subset of tests
* Automatically detect tests
* Skip tests
* Open source

`in terminal run`

```
pip install -U pytest
py.test -h
```
By default pytest only identifies the file names starting with `test_ `or ending with `_test` as the test files. We can explicitly mention other filenames though (explained later). Pytest requires the test method names to start with `"test."` All other method names will be ignored even if we explicitly ask to run those methods.

# Recursion

`recursion` -The process in which a function calls itself directly or indirectly

the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems.

If the base case is not reached or not defined, then the `stack overflow `problem may arise.

> `Tailed Recursive `- A recursive function is tail recursive when recursive call is the last thing executed by the function.



[Main Page](https://will-ing.github.io/reading-notes)
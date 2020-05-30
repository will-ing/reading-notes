# Pain and Growth

Consider these questions as you are struggling

1. What’s your perspective?
1. Why are you doing this?
1. Do you want what comes at the end of this journey?
1. Are you doing this for you?

> You’re in this class so that you can become not just a competent Python developer, but a spectacular craftsman of software with Python as your tool. The pain that you feel? Those are the callouses that you build while learning to use that tool.


## [Big O notation](https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation/)

> `Big O notation` is used in Computer Science to describe the performance or complexity of an algorithm.

`O(1) `describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

```
bool IsFirstElementNull(IList<string> elements)
{
    return elements[0] == null;
}
```

`O(N)` describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set. The example below also demonstrates how Big O favours the worst-case performance scenario; a matching string could be found during any iteration of the for loop and the function would return early, but Big O notation will always assume the upper limit where the algorithm will perform the maximum number of iterations.

```
bool ContainsValue(IList<string> elements, string value)
{
    foreach (var element in elements)
    {
        if (element == value) return true;
    }

    return false;
}
```

`O(N2)` represents an algorithm whose performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve nested iterations over the data set. Deeper nested iterations will result in O(N3), O(N4) etc.

```
bool ContainsDuplicates(IList<string> elements)
{
    for (var outer = 0; outer < elements.Count; outer++)
    {
        for (var inner = 0; inner < elements.Count; inner++)
        {
            // Don't compare with self
            if (outer == inner) continue;

            if (elements[outer] == elements[inner]) return true;
        }
    }

    return false;
}
```

`O(2N)` denotes an algorithm whose growth doubles with each additon to the input data set. The growth curve of an O(2N) function is exponential - starting off very shallow, then rising meteorically. An example of an O(2N) function is the recursive calculation of Fibonacci numbers:

```
int Fibonacci(int number)
{
    if (number <= 1) return number;

    return Fibonacci(number - 2) + Fibonacci(number - 1);
}

```


`Binary search` is a technique used to search sorted data sets.

[Facts and Myths about Python](https://www.youtube.com/watch?v=_AEJHKGk9ns)

[Python 3 module of the week](https://pymotw.com/3/index.html)


[How to set up a awesome Python environment](https://towardsdatascience.com/how-to-setup-an-awesome-python-environment-for-data-science-or-anything-else-35d358cc95d5)

[Main Page](https://will-ing.github.io/reading-notes)
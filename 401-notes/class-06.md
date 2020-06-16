# Random Module in Python

`Random Module` - provides access to functions that support many operations. Perhaps the most important thing is that it allows you to generate random numbers.

----
### Randint

Use it to get a random integer

```py
import random
print random.randint(0, 5)
```

----
### Random

For when you want a large number use multiply

```py
import random
random.random() * 100
```

---
### Choice

Generate random value form the sequence

```py
random.choice( ['red', 'black', 'green'] )
```

---
### Shuffle

Shuffles elements

```py
from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
```

---
### Randrange

Generate a random element from a range

```py
import random
for i in range(3):
    print random.randrange(0, 101, 5)
```
---
# Risk Analysis

>The probability of any unwanted incident is defined as Risk


[Main Page](https://will-ing.github.io/reading-notes)
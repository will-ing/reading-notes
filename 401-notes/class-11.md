# Jupyter

`JupyterLab` is a next-generation web-based user interface for Project Jupyter.

> JupyterLab enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner. 

```terminal
pip install jupyterlab
```

----

```terminal
jupyter notebook --version
```

----
Start jupyter

```terminal
jupyter lab
```

----

## Numpy

`NumPy` - is a commonly used Python data analysis package.

You can create a Numpy array using the numpy.array function.

First you have to import it

```py
import csv
with open("winequality-red.csv", 'r') as f:
    wines = list(csv.reader(f, delimiter=";"))
import numpy as np
wines = np.array(wines[1:], dtype=np.float)
```

numpy.genfromtxt function - Read the initial data

[Main Page](https://will-ing.github.io/reading-notes)
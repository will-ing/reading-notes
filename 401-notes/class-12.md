# Pandas

`Pandas` - is used to manipulate data

It supports many file formats out of the box.
works with tabular Data such as spreadsheets and databases

```py
import pandas as pd

nba = pd.read_csv("name.csv")

type(nba)

# you can see the length and size of the file using:
len(nba)

nba.shape
#return tuple (rows, col)

# to see the data you can use head to see the first five rows
nba.head()

# To display columns
pd.set_option("display.max.columns", None)

#to change the decimal places use
pd.set_option("display.precision", 2)

# to display the last 5 rows use:
nba.tail

#You can display all columns and their data types with .info():
nba.info()

```
[Main Page](https://will-ing.github.io/reading-notes)
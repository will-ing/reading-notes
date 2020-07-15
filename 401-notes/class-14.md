# Matplotlib

matpoltlib - provides both a very quick way to visualize data from Python and publication-quality figures in many formats

plyplot - the majority of plotting commands in pyplot have Matlab(TM) analogs with similar arguments.

```py
plt.figure(figsize=(10,6), dpi=80)
plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-")
plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-")
```

`Seaborn` - is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.

- lineplot() assumes that you are most often trying to draw y as a function of x, the default behavior is to sort the data by the x values before plotting.
- The default behavior in seaborn is to aggregate the multiple measurements at each x value by plotting the mean and the 95% confidence interval around the mean:
- The lineplot() function has the same flexibility as scatterplot(): it can show up to three additional variables by modifying the hue, size, and style of the plot elements.
- quick look at a univariate distribution in seaborn is the distplot() function.




[Main Page](https://will-ing.github.io/reading-notes)
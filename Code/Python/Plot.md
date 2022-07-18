## Plots
Routine
```python
fig, axes = plt.subplots(1, 2, figsize=(15, 6)) # 1 row, 2 plots
axes[0].scatter()
axes[1].plot()
plt.show()
```

Label and titles
```python
axes[0].set(xlabel='x label', ylabel='y label', title='Title')
axes[1].set(xlabel='x label', ylabel='y label', title='Title')
```

```python
plt.xlabel('x label')
plt.ylabel('y label')
plt.title('Title')
```

Heatmap (seaborn): 在作 confusion matrix 时用到，比 imshow 强大一点。这里主要用到在热图上标注的功能，是 imshow 没有的。
```Python
sns.heatmap(cm_accuracy, annot=cm,
xticklabels=['0.0','0.14','0.28','0.43','0.57','0.71','0.86','1.0'],
yticklabels=['0.0','0.14','0.28','0.43','0.57','0.71','0.86','1.0'])
```

Histogram 2d: 在作模拟的 snapshot 的可视化时用到
```python
hist, xedges, yedges, image = plt.hist2d(x, y, bins=64, density=False, norm=matplotlib.colors.LogNorm(), weights=None, range=None, cmin=None, cmax=None)
```


### Logarithmic axis
```Python
axe.set_yscale("log")
```

### Customize legend
```python
a, b = scatter.legend_elements()
b = [
    '$\\mathdefault{fSol = 0.0}$', 
    '$\\mathdefault{fSol = 0.2}$', 
    '$\\mathdefault{fSol = 0.4}$', 
    '$\\mathdefault{fSol = 0.6}$', 
    '$\\mathdefault{fSol = 0.8}$', 
    '$\\mathdefault{fSol = 1.0}$'
    ]
axes[0].legend(a, b)
```

## Common Configurations
`marker`
`label`
`color`
`linewidth`
`s`
`alpha`
`cmap`


## Notebook backends

https://github.com/microsoft/vscode-jupyter/wiki/Using-%25matplotlib-widget-instead-of-%25matplotlib-notebook,tk,etc

### Supported Backends:
VS code should work with these two options (has been thoroughly tested):

-   `%matplotlib inline` - This is the default and will render images as PNGs
-   `%matplotlib widget` - This generates an ipywidget that renders plots in a control. Multiple plots and zooming are supported. For more information see the [README](https://github.com/matplotlib/ipympl)

### Partially supported backends:

VS code may sometimes work with these options (has worked in some environments, but not others):

-   `%matplotlib qt5`
-   `%matplotlib agg`

### Unsupported backends (has been tried and fails/hangs):

-   `%matplotlib tk`
-   `%matplotlib notebook`
-   `%matplotlib nbagg`
-   `%matplotlib wx`
-   `%matplotlib svg`
-   `%matplotlib pdf`
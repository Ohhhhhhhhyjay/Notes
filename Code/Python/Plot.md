## Create plots
```python
fig, axes = plt.subplots(1, 2, figsize=(15, 6)) # 1 row, 2 plots
axes[0].scatter()
axes[1].plot()
plt.show()
```

## Customize legend
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
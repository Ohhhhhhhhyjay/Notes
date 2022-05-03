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

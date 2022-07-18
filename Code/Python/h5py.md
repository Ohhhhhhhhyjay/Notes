https://docs.h5py.org/en/stable/index.html

The most fundamental thing to remember when using h5py is:
**Groups work like dictionaries, and datasets work like NumPy arrays.** 

"HDF" stands for "Hierarchical Data Format". Every object in an HDF5 file has a name, and they’re arranged in a POSIX-style hierarchy with `/`-separators. The “folders” in this system are called groups.

```python
import h5py
f = h5py.File('file.hdf5', 'r')
```

We here use the format of [[IllustrisTNG Data]] as examples.
## Groups
### Methods
`keys()`
`values()`
`items()` : {'key' : value}
可用 for 循环遍历
## Datasets
### Attributes
`shape`
`size`
`ndim`
`dtype`
`nbytes`
### Indexing
`f['PartType0'][()]` , `f['PartType0'][...]` , `f['PartType0'][:]` : returns the array of the data
Supports most (probably all) Numpy fancy indexing and slicing.


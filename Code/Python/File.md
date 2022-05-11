https://zhuanlan.zhihu.com/p/95989702

File Mode        Meaning

`r` Opens a file for reading (default)

`w` Open a file for writing. If a file already exists, it deletes all the existing contents and adds new content from the start of the file.

`x` Open a file for exclusive creation. If the file already exists, this operation fails.

`a` Open a file in the append mode and add new content at the end of the file.

`b` Open the file in binary mode.

`t` Opens a file in a text mode (default).

`+` Open a file for updating (reading and writing).

## Opening a file

```python
with open('filename') as file:
	data = file.read()
```

```python
with open('filename') as f: 
     for line in f: 
         print(line)
```


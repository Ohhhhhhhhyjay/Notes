### Basic Operations
算术运算符一共有6种，除了加减乘除外还有余数和整数除法。
`+, -, *, /, %, //`

#### `from <module> import *` 
import all functions in `<module>`. One can refer to them directly (instead of `<module>.<function>`).

#### `if __name__ == '__main__':` 的作用
一个python文件通常有两种使用方法，第一是作为脚本直接执行，第二是 `import` 到其他的 python 脚本中被调用（模块重用）执行。因此 `if __name__ == 'main':` 的作用就是控制这两种情况执行代码的过程，在 `if __name__ == 'main':` 下的代码只有在第一种情况下（即文件作为脚本直接执行）才会被执行，而 `import` 到其他脚本中是不会被执行的。

#### python中的map()函数
`map()` 是 Python 内置的高阶函数，它接收一个函数 `f` 和一个 `list`，并通过把函数 `f`依次作用在`list` 的每个元素上，得到一个新的 `list` 并返回一个 `map object`. 可以用 `list()` 将 `map object` 转化为想要的 `list`.
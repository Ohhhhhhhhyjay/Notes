矩阵乘法
`np.matmul(a,b)`
`np.dot(a,b)`

向量的模
`np.linalg.norm(x)``

### Indexing and Slicing
`arr[2::3]` : 从第2个元素开始，每3个元素取一个

#### `np.meshgrid` 的功能
从坐标节点创造向量场。从 shape 分别为 (10,), (10,), (10,) 的格点N1, N2, N3数组，创建出 shape 为 (3,10,10,10) 的坐标向量场（位置矢量）
![[Pasted image 20220624010612.png]]
需要注意的是，这里有一个参数 `indexing` 默认 `indexing='xy'` 此时向量场的坐标为 `[N2,N1,N3]` ，可选设置为 `indexing='ij'` 则向量场为 `[N1,N2,N3]`. 不知道为什么会默认第一种设置. 不知道什么情境下会用到.


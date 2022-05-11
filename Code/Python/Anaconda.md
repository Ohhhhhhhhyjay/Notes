## Manage environments
经验：
1. 如果出现问题，就新建一个环境然后换换安装顺序。
2. 尝试寻找整合好的解决方案，比如 Anaconda 就能解决许多 pip 解决不了的问题。

```shell
conda env list
conda create --name <myenv> python=3.6
conda env remove --name <myenv> # remove an environment
conda install -c conda-forge sunpy # install from conda-forge channel. go to anaconda.org for additional info
```

版本回滚。如果一不小心在 `base` 之类的不想要的地方装了包。

```shell
conda list --revisions
conda install --revision <number>
```

## Environments
### For WST
We use [Kymatio](<https://www.kymat.io/>) package.

>Certain frontends, `numpy` and `sklearn`, only allow processing on the CPU and are therefore slower. The `torch`, `tensorflow`, and `keras` frontends, however, also support GPU processing, which can significantly accelerate computations. Additionally, the `torch` backend supports an optimized `skcuda` backend which currently provides the fastest performance in computing scattering transforms.
>
>To run Kymatio on a graphics processing unit (GPU), you can either use the PyTorch-style `cuda()` method to move your object to GPU. Kymatio is designed to operate on a variety of backends for tensor operations. For extra speed, install the CUDA library and the `skcuda` dependency by running the following pip command:

This is the success install sequence I used in the end

```shell
conda env remove --name moria
conda create --name moria python=3.6
conda activate moria

conda install pytorch torchvision torchaudio cudatoolkit=11.2 -c pytorch
conda install -c conda-forge pycuda
pip install scikit-cuda
conda install -c anaconda cupy

pip install kymatio sklearn scikit-image seaborn jupyter

```

My
Torch version: 1.10.2
CUDA version: 10.2
cuDNN version: 7605


On installing pycuda (when installing `scikit-cuda`:
`pip install pycuda --no-binary :all:`  does not work
`conda install -c conda-forge pycuda` does the job
Anaconda永远的神


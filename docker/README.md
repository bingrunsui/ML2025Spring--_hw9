# PEFT Docker 镜像

这里存放了我们测试基础设施中使用的所有 PEFT Docker 镜像。目前我们所有镜像均使用 Python 3.8。

- `peft-cpu`：在 CPU 上编译的 PEFT，并安装了主分支上的所有其他 HF 库
- `peft-gpu`：为 NVIDIA GPU 编译的 PEFT，并安装了主分支上的所有其他 HF 库
- `peft-gpu-bnb-source`：为 NVIDIA GPU 编译的 PEFT，`bitsandbytes` 及所有其他 HF 库均从主分支安装
- `peft-gpu-bnb-latest`：为 NVIDIA GPU 编译的 PEFT，`bitsandbytes` 从主分支编译，所有其他 HF 库从最新的 PyPi 安装
- `peft-gpu-bnb-multi-source`：为 NVIDIA GPU 编译的 PEFT，`bitsandbytes` 从 `multi-backend` 分支编译，所有其他 HF 库从主分支安装

`peft-gpu-bnb-source` 和 `peft-gpu-bnb-multi-source` 本质上是一样的，唯一的区别是 `bitsandbytes` 编译自不同的分支。请确保你在其中一个文件上做的更改也同步到另一个文件！

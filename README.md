# 微软 GraphRAG 的部署与调用

## 配置环境

1. **创建虚拟环境**
```sh
conda create -n graphrag python=3.11 -y
conda activate graphrag
```

2. **安装并配置 Jupyter Kernel**
* 安装 JupyterLab 和 IPython 内核：
```sh
conda install jupyterlab
conda install ipykernel
```
* 将当前虚拟环境注册到 jupyterlab 内核：
```sh
python -m ipykernel install --user --name graphrag --display-name "Python (graphrag)"
```
* 启动 jupyterlab：
```sh
jupyter lab --no-browser --port=8888 --allow-root
```
* 如果使用的是远程的 jupyter 服务器，则需要在本地电脑建立 SSH 端口转发：
```sh
ssh -L 8888:localhost:8888 root@远程服务器IP
```

3. **安装依赖**
```
pip install graphrag==0.5.0
pip install --upgrade jupyter ipywidgets
```

> 本实验环境基于 Ubuntu 系统。大多数操作方法亦可直接迁移至 Windows 系统。

## GraphRAG 的使用
- [GraphRAG 快速部署与调用](./graphrag_quick_start.ipynb)

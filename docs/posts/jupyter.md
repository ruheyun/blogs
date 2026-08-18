
## Jupyter 安装 
如果通过 `vscode` 或者 `pycharm` 运行 `jupyter notebook` 只需安装下面这个包即可
```
pip install jupyterlab
```

如果需要在浏览器打开 `jupyter notebook` ，除了安装上面的包外还需安装下面的包
```
pip install ipykernel
```
并且需要在安装上述两个包的环境中，注册内核
```
python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
```

参数解释：

`python -m ipykernel` 以模块方式运行 `ipykernel` 

`install` 注册一个内核到 `jupyter` 中

`--user` 按用户安装，而非系统全局，无需管理员权限。内核规格会写入 `~/.local/share/jupyter/kernels/`（Linux/macOS）或 `%APPDATA%/jupyter/kernels/`（Windows）

`--name myenv` 内核的内部标识名，必须唯一。该名称用于 `jupyter` 内部识别，用户看不到

`--display-name "Python(myenv)"` 在浏览器 `jupyter` 界面显示的名称，用户在下拉内核菜单中看到的名称

> 上述注册内核命令中，可以自定义的是 `myenv` 和 `"Python(myenv)"` 。

## 使用
如果是 `vscode` 或者 `pycharm` 中，只需要打开 `jupyter notebook` ，然后选择激活的环境名称即可；

如果是浏览器打开， 则需要在命令行窗口（cmd）里先激活环境，再输入 `jupyter notebook` 即可自动跳转浏览器打开，并且打开路径是命令行窗口中执行命令的路径
```
conda activate python3.12  # 先激活安装了上述两种包的环境

jupyter notebook  # 打开jupyter
```

## 删除内核
如果不再需要使用浏览器打开 `jupyter` 则可以使用下述命令删除注册的内核
```
jupyter kernelspec remove myenv
```
这个命令里，`myenv` 是注册内核时对应的 `--name` 的参数设置。注意这里只是删除内核，上述安装的包，以及环境都没有删除。


## 转换md文件

需要先安装两个依赖包
```
pip install nbconvert pandoc
```

然后使用下面命令即可
```
jupyter nbconvert --to <format> <notebook>.ipynb
```

> [!tip]
> 1. format: 需要转换的格式，比如 markdown、html、py
> 2. notebook: 替换为你 jupyter notebook 的名字
> 3. 会在当前文件夹下生成文档


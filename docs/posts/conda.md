## 基本使用命令

以下命令（代码）需要再 `cmd` 里输入。

1. 查看 conda 版本

```
conda --version
```

2. 更新 conda

```
conda update conda
```

3. 查看已创建的虚拟环境

```
conda env list
```

> 星号（*）代表当前激活的环境

4. 创建新环境

```
conda create --prefix path python=version
```

> path 是包含新环境名的绝对路径

```
conda create -n name python=version
```

> 如果在默认路径下创建新环境，则常用这个命令
>
> name 新环境名字

5. 激活环境（切换环境）

```
conda activate name
```

6. 回退到默认根环境

```
conda deactivate
```

7. 删除环境

```
# 先退出要删除的环境，再用下面命令，path 指包含环境名字的绝对路径
conda env remove -p path

# 或者使用下面命令，name 指环境名字
conda remove -n name --all
```

## 对模块进行操作

模块的增删改查是根据当前激活的虚拟环境进行的，即带星号的环境。（这里的模块指的是 Python 中的包）

1. 搜索模块

```
conda search name
# 比如：conda search requests
```

2. 下载模块

```
conda install name

# 或者指定版本
conda install name=version

# 不过更建议使用 pip 安装 Python 包
pip install name

# 或者指定版本
pip install name==version
```

3. 查看当前环境已下载模块

```
conda list

# pip 命令
pip list
```

4. 升级模块

```
conda update name

# 或者升级所有模块
conda update --all

# 或使用 pip 升级模块
pip install --upgrade name
```

5. 删除模块

```
conda remove name
```

## 其他操作

```
# 更新基础环境中的conda
conda update -n base -c defaults conda

# 显示conda环境的安装源
conda config --show-sources

# 添加国内镜像源
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/nvidia

http://mirrors.aliyun.com/pypi/simple

# add（添加到前面） 可以用 append（添加到最后）替换

# 移除某一个安装源
conda config --remove channels  https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge 

# 移除所有源
conda config --remove-key channels

# conda安装较慢，使用mamba加速，安装mamba
conda install -n base -c conda-forge mamba

# 将mamba加入环境配置
mamba shell init --shell bash --root-prefix=~/.local/share/mamba

mamba shell init --root-prefix=/root/miniconda3 --shell=bash
source ~/.bashrc


# 将以上环境设置好后，重新加载一下配置
source ~/.bashrc

# 使用mamba激活环境
mamba activate /root/autodl-tmp/envoriment/RAPID

# 将conda安装源从上到下的严格顺序改为灵活选择
conda config --set channel_priority flexible

conda config --show | grep channel_priority

conda config --set show_channel_urls yes

# 所有环境安装好后可以使用pip check检查是否有包冲突
pip check

# 如下面两个包冲突，使用下面命令让pip自选择适合的包
pip install "altair<5.4.1" "typing-extensions==4.5.0"

#清除所有缓存
sudo conda clean --all
```

## jupter 使用

```
# jupter notebook使用
pip install jupyterlab

# 如果想要在浏览器打开jupter notebook使用conda环境需要注册内核（kernel）
pip install ipykernel
python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
```
> 🕒 本文最后更新：{docsify-updated}
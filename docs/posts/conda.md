# Conda 笔记

以下命令（代码）需要再 `cmd` 里输入。

## 安装
[miniconda安装教程](https://docs.anaconda.net.cn/miniconda/install/)
> 正常使用安装 `miniconda` 即可，不需要安装 `anaconda`。

## 常用命令
**查看 `conda` 版本**
```
conda --version
```

**更新 `conda`**
```
conda update conda
```

**查看已创建的 `conda` 环境**
```
conda env list
```
> 对于新安装的 `conda` 只有一个默认的环境，为 `base` 。如果 `conda` 环境激活，则默认激活 `base` 环境。环境名前面显示的`星号`表示当前环境被激活。

**创建新环境**
（路径安装法，需要替换 `my_path` `version` 为具体值）
```
conda create --prefix my_path python=version
```
（名称安装法，需要替换 `my_name` `version` 为具体值）
```
conda create -n my_name python=version
```
> 名称安装法创建新环境命令，将安装在默认的文件夹，建议使用名称安装法这种创建方式。

**激活环境**
```
conda activate my_name
```
> 如果使用上述路径安装法则需要在名称前加上绝对路径。

**回退默认环境**
```
conda deactivate
```
或者换个思路，等价于激活默认环境
```
conda activate base
```

**删除环境**

需要先退出要删除的环境，再用下面命令
```
conda env remove -n name --all
```
或者
```
conda env remove -p path
```

## 模块操作
模块的增删改查是根据当前激活的虚拟环境进行的，即带星号的环境。（这里的模块指的是 Python 中的包）

**搜索模块**
```
conda search name
```
> 比如：conda search requests
  
**下载模块**
```
conda install name
```
或者指定版本
```
conda install name=version

# 使用 pip 安装
pip install name==version
```
  
**查看当前环境已下载模块**
```
conda list
```

**升级模块**
```
conda update name

# 或使用 pip 升级模块
pip install --upgrade name
```
或者升级所有模块
```
conda update --all
```
  
**删除模块**
```
conda remove name
```
> 上述操作 `python` 包的命令都可以将命令中的 `conda` 换成 `pip` 会加速下载。

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

conda config --add channels http://mirrors.aliyun.com/pypi/simple

# add（添加到前面） 可以用 append（添加到最后）替换

# 移除某一个安装源
conda config --remove channels  https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge

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
> 如果网络好，不建议更换镜像源。
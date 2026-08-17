# Pytorch笔记

[Pytorch官网](https://pytorch.org/get-started/locally/)

[历史版本网站](https://pytorch.org/get-started/previous-versions/)

## torch安装
这里以历史版本 `2.5.1` 为例，进入历史版本网站，找到 `v2.5.1`，复制命令安装即可
```
pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1 --index-url https://download.pytorch.org/whl/cu118
```
> 后面带 `cu` 表示安装的是 `gpu` 版本

```
pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1

# 或者

pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1 --index-url https://download.pytorch.org/whl/cpu
```
> 默认是 `cpu`，或者指定版本为 `cpu`

> 记得激活指定的 `conda` 环境，不然会安装到默认环境里，造成不同版本的冲突。

## 测试
安装完成后，可以在命令行，先输入 `python` 进入`python的交互式编程模式`，然后依次输入下面代码

**导入torch**
```
import torch
```

**查看pytorch安装版本号**
```
print(torch.__version__)
```

**查看cuda是否可用，即判断是gpu还是cpu的pytorch**
```
print(torch.cuda.is_available())
```

**返回gpu型号**
```
print(torch.cuda.get_device_name(0))
```

**返回gpu的数量**
```
print(torch.cuda.device_count())
```

**查看cuda版本**
```
print(torch.version.cuda)
```

**检查cudnn是否可以用**
```
print(torch.backends.cudnn.version())
```

```
from torch.backends import cudnn
```

```
cudnn.is_available()
```

## 保存/加载模型权重
```
# pytorch中模型的保存与加载
# 1.保存模型权重
torch.save(teacher.state_dict(), "teacher_model.pth")
# 2.加载模型权重
teacher = TeacherModel()  # 重新实例化模型
teacher.load_state_dict(torch.load("teacher_model.pth"))
teacher.eval()  # 切换到评估模式
```

**自定义保存路径**
```
# ---------------保存到自定义路径------------------------
import os
import torch

# 定义保存路径
save_dir = "./models/"
os.makedirs(save_dir, exist_ok=True)  # 如果目录不存在则创建

# 定义保存文件路径
save_path = os.path.join(save_dir, "teacher_model.pth")

# 保存模型权重
torch.save(teacher.state_dict(), save_path)
print(f"模型已保存到: {save_path}")
```

## 保存/加载模型
```
# 1.保存模型
torch.save(teacher, "teacher_full_model.pth")
# 2.加载模型, 不需要重新实例化即可加载
teacher = torch.load("teacher_full_model.pth")
teacher.eval()
```

> 保存模型权重与保存模型的区别在于，保存模型权重不会保存网络结构，因此文件占用会比较小，建议只保存模型权重。


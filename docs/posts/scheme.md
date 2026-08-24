# MIT/GNU Scheme 安装

本安装笔记记录了 `MIT/GNU Scheme` 在 Windows11 下的安装过程。

**1.下载exe版本安装包**

由于[官网](https://www.gnu.org/software/mit-scheme/)最新版本不再支持 Windows 系统，因此需要去下载老版本的安装包：[历史版本](https://ftp.gnu.org/gnu/mit-scheme/stable.pkg/)。

这里以[9.2版本](https://ftp.gnu.org/gnu/mit-scheme/stable.pkg/9.2/)为例，进行下载安装。

> 9.2版本是最后一个支持 Windows 的版本

进入 9.2版本 界面，点击 `mit-scheme-9.2-i386-win32.exe` 进行下载。

**2.安装 Scheme**

直接双击安装包，一路默认 `next` 即可。

然后桌面会出现一个快捷方式 `MIT-GNU Scheme` ，右键点击该快捷方式，选择属性，然后将 `目标(T)` 里的内容：

`"C:\Program Files (x86)\MIT-GNU Scheme\bin\mit-scheme.exe" --library "C:\Program Files (x86)\MIT-GNU Scheme\lib" --edit`

改为下面内容

`"C:\Program Files (x86)\MIT-GNU Scheme\bin\mit-scheme.exe" --library "C:\Program Files (x86)\MIT-GNU Scheme\lib" --heap 512 --edit`

最后点击应用——保存，双击快捷方式可以打开软件进行使用。

> 如果在安装过程中更改了默认安装路径，则这里的内容也应改为对应的路径。


#anaconda #cuda #深度学习

入门深度学习，首先要做的事情就是要搭建深度学习的环境。不管你是Windows用户，Mac用户还是Ubuntu用户，只要电脑配置允许，都可以做深度学习，毕竟Windows、Mac和Ubuntu系统都可以进行深度学习环境的搭建。接下来就记录下自己在Windows系统上搭建深度学习环境的过程，方便自己存档也为大家提供一个参考。  
本次环境配置主要模式是基于**Anaconda+PyTorch(GPU版)+CUDA+cuDNN**进行搭建的。
## 大纲 
1. 安装Anaconda
2. 安装Nvidia驱动
3. 安装CUDA TOOls
4. 安装cuDNN
5. 安装pytorch

## 1.安装Anaconda
### 1.1 下载
Anaconda官网：[https://www.anaconda.com](https://www.anaconda.com/)
![[Pasted image 20231018185315.png|725]]
### 1.2 安装
击下载后的.exe文件进行安装。安装一般没有大问题，一直点next就行。
此处如果电脑只有你一个用户的话，也可以选择Just Me; 选择All Users就代表这台电脑上的所有用户均可使用，否则就需要管理员权限。一般选择All Users即可。  
![在这里插入图片描述](https://img-blog.csdnimg.cn/ef1f8cfa719b478c97cd4d079a07920d.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5YKy5a-S44CC,size_20,color_FFFFFF,t_70,g_se,x_16#pic_center)  
![在这里插入图片描述](https://img-blog.csdnimg.cn/daedf03a99cf47c1b0f9527f772323b8.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5YKy5a-S44CC,size_20,color_FFFFFF,t_70,g_se,x_16#pic_center)  
_**此处注意：文件夹必须是空的，不然会报错；其次文件夹名称中不要出现中文字符。**_  
![在这里插入图片描述](https://img-blog.csdnimg.cn/9312dc2d259c4ed386391143e3ddeae8.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5YKy5a-S44CC,size_20,color_FFFFFF,t_70,g_se,x_16#pic_center)  
然后安装即可。  
### 1.3 添加环境变量
在安装完Anaconda之后，打开CMD终端，输入`conda`会出现`command not found`这是由于电脑未添加Anaconda运行环境。

在`我的电脑->属性->高级系统设置->环境变量`中添加命令
![[Pasted image 20231018190020.png|550]]

双击Path后点击浏览，选择Anaconda的安装目录，选择Anaconda安装目录下的Scripts文件夹即可
![[Pasted image 20231018190057.png|500]]

关闭终端，重新打开后输入`conda`，命令生效

## 2.安装NVIDIA驱动
这个步骤，笔者的驱动都是自动更新的，没有手动安装，想要手动安装可以去[英伟达官网](https://www.nvidia.cn/geforce/drivers/)下载
## 3.安装CUDA
在终端中输入`nvidia-smi`，可以看见自己显卡的相关信息。  
![[Pasted image 20231018191041.png|475]]
其中Driver Version是你的英伟达显卡驱动版本，CUDA Version是你的CUDA对应版本，我们要去[CUDA官网](https://developer.nvidia.com/cuda-downloads)下载不高于这个版本的CUDA，下载完成后，一路安装即可。

## 3.安装cuDNN
从这里下载[cuDNN](https://developer.nvidia.com/rdp/cudnn-download)，下载时注意，版本需要和CUDA版本保持一致。
![[Pasted image 20231018191749.png|500]]
下载完成后，得到一个压缩包，解压后获得如下文件夹
![[Pasted image 20231018191837.png|500]]
前往CUDA的文件夹（不是安装目录）下：`C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.2`
![[Pasted image 20231018192130.png|500]]
将文件夹中的文件，与CUDA一一对应拖动进去即可
至此，CUDA就安装完成了，打开CMD，输入`nvcc -V`，如果有输出即可。

## 安装pytorch
经历了以上几步，我们终于配置好了显卡的驱动相关，接下来我们开始安装pytorch。 
首先需要创建一个虚拟环境，然后进入我们创建好的的pytorch环境，输入以下命令：
创建名叫pytorch的虚拟环境：
```bash
conda create -n pytorch python=3.9
```
进入pytorch虚拟环境：
```bash
conda activate pytorch
```
然后安装pytorch：
```bash
conda install pytorch
```
之后等待solving environment，好了以后按照提示按y回车，就自动装好了  
来验证一下我们装的是否有效。
即首先用`conda activate pytorch`进入pytorch虚拟环境，然后在终端输入python进入python界面
分别输入
```bash
import torch
torch.cuda.is_available()
```

![[Pasted image 20231018194305.png]]
import torch以后回车无error，第二行指令返回的是true就大功告成，
但是，笔者这里返回的是False，采用如下方法
**换了种方法，如下：**  
PyTorch官网：https://pytorch.org
官网界面往下拉  
![[Pasted image 20231018194752.png]]
选择自己电脑的相关配置，然后在anaconda prompt中运行Run this Command里的代码，等待运行一段时间之后，重新运行上面的`torch.cuda.is_available()`，返回True！
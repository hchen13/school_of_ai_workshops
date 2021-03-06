# 环境搭建

在正式开始我们的深度学习开发之前, 我们需要先安装开发环境. 

视频教程: [优酷](https://v.youku.com/v_show/id_XNDE2NDUwNzczMg==.html?spm=a2h3j.8428770.3416059.1)

## 1. Python 3

### 安装conda

若已经安装过conda, 请略过这部分.

一种简单的方式是用[miniconda](https://docs.conda.io/en/latest/miniconda.html)来安装Python语言, 
通过它可以方便的创建虚拟环境, 管理Python版本和各种库类等. 下面以Mac OS X系统为例, 先下载安装文件, 下载完成后执行脚本
 (Windows用户可通过上面网站下载exe安装包进行安装):
~~~bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
bash Miniconda3-latest-MacOSX-x86_64.sh
~~~

安装完毕后根据提示需要重启terminal或者手动加载才能使用: 
~~~bash
source ~/.bash_profile
~~~

验证安装:
~~~bash
conda -h
~~~

### 安装python3.6.5环境

创建虚拟环境并查看已经安装了的所有环境, 若已经创建过python 3.6.5的环境请略过:
~~~bash
conda create -n deeplearning python=3.6.5 matplotlib -y
conda-env list
~~~

进入到所创建的deeplearning环境开始使用
~~~bash
conda activate deeplearning
~~~

\* **用```conda deactivate```命令来结束使用环境.**

## 2. 依赖

在开发中我们会用到各种库类依赖, 需要先把他们安装起来, 这里是在安装python能使用的依赖.

**重点**

**所以在进行这一步之前, 一定要先```conda activate deeplearning```进入到我们的
deeplearning环境中, 否则下列安装不能在我们的环境中生效.**

~~~bash
pip install scikit-image opencv-contrib-python numpy tensorflow==1.11.0 keras -i https://pypi.doubanio.com/simple/
~~~

在上面的命令中, 我们通过豆瓣的镜像源下载了scikit-image, opencv, numpy, tensorflow, keras这几个开发库. 不同的项目需要不同的库类, 根据需要安装即可

在深度学习开发中的常用库类:

* tensorflow
* keras
* numpy
* scikit-learn
* scikit-image
* opencv-contrib-python
* pillow
* pandas
* jupyter
* jupyterlab
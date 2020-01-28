# pip使用

```shell
# 输出已安装的库
pip list

#显示某个已安装库的信息
pip show xxxx
## eg:
pip show numpy

# Search PyPI for packages
pip saarch xxxx
## eg:检查目前有哪些版本的tensorflow可以安装
pip search tensorflow
```



```shell
# 代表进行全局安装，安装后全局可用。如果是信任的安装包可用使用该命令进行安装
pip install packagename


# 代表仅该用户的安装，安装后仅该用户可用。处于安全考虑，尽量使用该命令进行安装
pip install --user packagename
## 安装tensorflow的时候要用熵 --user 这个参数

## 安装指定版本的tensorflow
pip install tensorflow==1.15
```



## 使用文本安装

1. 新建文档`requirements.txt`

2. 文档写入（也就是想要库的对应版本），比如：

   ```shell
   numpy==1.14.5
   Pillow==5.2.0
   scipy==1.1.0
   six==1.11.0
   tensorflow==1.4.0
   ```
3. 对应环境中运行`pip install -r requirements.txt` 




# conda使用

```shell
#查看帮助
conda env --help

#列出所有的虚拟环境
conda env list
conda info --envs

#查看指定虚拟环境下的package
conda list --name [虚拟环境名]   

#创建
conda create --name [虚拟环境名] [python的版本] [需要的包]

## eg:
conda create --name myenv
conda create --name myenv python=2.7
conda create --name myenv pytohon=2.7 numpy scipy

#克隆
conda create --name [虚拟环境名] -- clone [colne的环境]

## eg:
#创建一个和原python环境一样的虚拟环境
conda create --name mybase --clone base

#删除
conda remove --name [虚拟环境名] -all

 

# 激活取消（默认的环境是base）
activate [虚拟环境名]

deactivate [虚拟环境名]

 

# 虚拟环境激活后，在cmd中输入python，显示的就是一个新的环境。

```



```shell
# 检查目前有哪些版本的python可以安装：
conda search --full-name python

# 检查目前有哪些版本的tensorflow可以安装：
conda search --full-name tensorflow
```



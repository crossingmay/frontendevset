## Python

### 安装


为了不污染系统自带的Python，我们得通过homebrew安装属于私有的Python

`$ brew install python`

装完之后通过`$ which python`查看所在目录应该在`/usr/local/bin/python`

这种方法装完python之后同时也会把**Pip**(依赖**Setuptools**)装好.

```
$ pip install --upgrade setuptools
$ pip install --upgrade pip
```

### Pip Usage

安装包:`$ pip install <package>`

更新包:`$ pip install --upgrade <package>`

查看包:`$ pip freeze`

卸载包:`$ pip uninstall <package>`

### Virtualenv

Install:`$ pip install virtualenv`

Usage:

建立一个虚拟目录

```
$ cd myproject/
$ virtualenv venv --distribute
```

如果需要继承全局环境下安装的包，使用

`$ virtualenv venv --distribute --system-site-packages`


首先需要激活一下：`$ source venv/bin/activate`

然后再运行`$ pip install <package>`，就会安装到`venv`文件夹里，并且不会影响到其他项目。

`$ deactivate`离开虚拟环境。

*Important:*记住在`venv`里添加`.gitignore`文件，避免源代码混入奇怪的东西。

### [Virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/en/latest/install.html)

安装:`$ pip install virtualenvwrapper`

```
export WORKON_HOME=$HOME/.virtualenvs
export PROJECT_HOME=$HOME/Devel
source /usr/local/bin/virtualenvwrapper.sh
```
在`.zshrc`中的这段就是这里的配置信息



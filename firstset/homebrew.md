## Homebrew

ps：打开终端运行(CMD+T可新建tab页)

### 安装



```
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

```

### 环境变量设置

```
$ echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile

```


### 基本使用

安装一个包：`$  brew install <package_name>`

更新包目录：`$ brew update`

如果更新命令失败，我们可以尝试用下面的代码：

```
$ cd /usr/local
$ git fetch origin
$ git reset --hard origin/master
```

查看是否需要更新：`$ brew outdated`

更新包：`$ brew upgrade <package_name>`

清理旧版本包缓存：`$ brew cleanup`

查看安装过的包列表：`$ brew list --versions`

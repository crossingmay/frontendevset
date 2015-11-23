## iTerm2&zsh

### 安装iterm2和zsh

安装iterm2终端:`brew cask install iterm2`

设置快捷键：隐藏和显示的快捷键

安装zsh:`brew install zsh zsh-completions`

改变默认shell:`chsh -s /bin/zsh`

### zsh个性化设置

装完zsh之后，安装oh-my-zsh:

```
curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh
```

安装主题：下载 [Solarized dark iterm colors](https://github.com/altercation/solarized/tree/master/iterm2-colors-solarized)，在 Profiles -> Default -> Colors -> Load Presets 将其导入，作为默认颜色。


使文字颜色生效：在Preference -> Text -> Text Rendering -> uncheck Draw Bold

### 配置文件

编辑`.zshrc`

```
ZSH_THEME=pygmalion
# Use sublimetext for editing config files
alias zshconfig="subl ~/.zshrc"
alias envconfig="subl ~/Projects/config/env.sh"
plugins=(git colored-man colorize github jira vagrant virtualenv pip python brew osx zsh-syntax-highlighting)
alias -s html=subl   # 在命令行直接输入后缀为 html 的文件名，会在 sublime 中打开
alias -s rb=subl     # 在命令行直接输入 ruby 文件，会在 sublime 中打开
alias -s py=subl       # 在命令行直接输入 python 文件，会用 sublime 中打开，以下类似
alias -s js=subl
alias -s txt=subl
```
`env.sh` 用于维护别名（aliases），输出（exports）和路径改变（path changes）等等，以免影响 ~/.zshrc

（Ps:需要brew install添加python和ruby模块，并且不能另外再安装python在外面（除系统自带的python和ruby以外）否则运行会出错:virtualenvwrapper.sh不会在该在的目录下。

```
    #!/bin/zsh

    # PATH
    export PATH="/usr/local/share/python:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin"
    export EDITOR='subl -w'
    # export PYTHONPATH=$PYTHONPATH
    # export MANPATH="/usr/local/man:$MANPATH"

    # Virtual Environment
    export WORKON_HOME=$HOME/.virtualenvs
    export PROJECT_HOME=$HOME/Projects
    source /usr/local/bin/virtualenvwrapper.sh

    # Owner
    export USER_NAME="YOUR NAME"
    eval "$(rbenv init -)"

    # FileSearch
    function f() { find . -iname "*$1*" ${@:2} }
    function r() { grep "$1" ${@:2} -R . }

    #mkdir and cd
    function mkcd() { mkdir -p "$@" && cd "$_"; }

    # Aliases
    alias cppcompile='c++ -std=c++11 -stdlib=libc++'
```
### 参考链接

**iTerm2使用:**[iTerm2使用指南](http://pengjunjie.com/articles/mac-soft-iterm2/)

**zsh使用:**池建强[终极shell](http://macshuo.com/?p=676)

**Important:** 新增、修改环境变量，都需要source；删除则需要重启终端。
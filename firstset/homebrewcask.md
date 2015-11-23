## Homebrew Cask

### 安装

使用cask安装管理OSX**图形界面程序**:

```
$ brew install caskroom/cask/brew-cask
$ brew cask install google-chrome
```
或者

```
$ brew tap caskroom/cask  // 添加 Github 上的 caskroom/cask 库
$ brew install brew-cask  // 安装 brew-cask
$ brew cask install google-chrome // 安装 Google 浏览器
$ brew update && brew upgrade brew-cask && brew cleanup // 更新
```

### 搜索

搜索app是否支持brew cask 安装可查看：[caskroom.io](http://caskroom.io/)

### quicklook 插件

**语法高亮、markdown渲染、json预览等**

常用[quicklook插件](https://github.com/sindresorhus/quick-look-plugins)安装

[QuickLook Plugins List](http://www.quicklookplugins.com/)

**How to Install**

把`*.qlgenerator`文件复制到`/Library/QuickLook/`或`~/Library/QuickLook/`目录下

然后在终端输入`$ qlmanage -r`将会搜索上述目录下的新增ql插件，并载入



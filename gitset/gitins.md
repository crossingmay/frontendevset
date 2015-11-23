## git
安装:`brew install git`

通过`which git`来确定安装在目录`/usr/local/bin/git`


git设置:这些信息都会被添加到`.gitconfig`

```
# 设置用户名和邮箱，同github
$ git config --global user.name "Your Name Here"
$ git config --global user.email "your_email@youremail.com"
# 读取osx里的密码，不用每次都输入帐号密码
$ git config --global credential.helper osxkeychain
```

设置sublime作为默认的mergetool

```
$ git config --global mergetool.sublime.cmd "subl -w \$MERGED"
$ git config --global mergetool.sublime.trustExitCode false 
$ git config --global merge.tool sublime
$ git mergetool -y
```

创建 `~/.gitignore`设置`.gitignore`

```
# Folder view configuration files
.DS_Store
Desktop.ini

# Thumbnail cache files
._*
Thumbs.db

# Files that might appear on external disks
.Spotlight-V100
.Trashes

# Compiled Python files
*.pyc

# Compiled C++ files
*.out

# Application specific files
venv
node_modules
.sass-cache
```

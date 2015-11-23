## Ruby

同样的，为了不污染系统自带ruby，我们得自己再通过homebrew安装一个ruby

```
$ brew install rbenv ruby-build rbenv-gem-rehash rbenv-default-gems
$ echo 'eval "$(rbenv init -)"' >> ~/Projects/config/env.sh
$ sourcezsh
```

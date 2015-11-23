## 安装和配置

### 安装

```
brew tap caskroom/versions
brew cask install sublime-text3
```

### 配置

配置信息分为`Default`和`User`两个版本，通过修改`User`的配置来完成个性化配置

### Package Control 安装

* [Install Package Control](https://packagecontrol.io/installation)

通过*ctrl+`*打开控制台，输入以下代码


```
import urllib.request,os,hashlib; h = '2915d1851351e5ee549c20394736b442' + '8bc59f460fa1548d1514676163dafc88'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

## nvm 安装

**方法一:**


用`$ brew install nvm`安裝nvm
	
这个时候需要注意这个问题，重启终端，node系统环境变量会失效，所以需要下面的步骤。
	
`$ brew info nvm`会输出一段信息，根据提示操作

1. 创建 .nvm 文件:`mkdir ~/.nvm`

2. 然后把 nvm-exec 文件拷贝到新建的 .nvm 目录下

	`cp $(brew --prefix nvm)/nvm-exec ~/.nvm/`

3. 然后去编辑`bash`配置文件`$ ~/.bash_profile`,
		
	如果使用`zsh`那么编辑 `$~/.zshrc`配置文件
		
	`open ~/.bash_profile`或`open ~/.zshrc`

4. 把下面的内容粘贴进去
	
	```
	export NVM_DIR=~/.nvm
	source $(brew --prefix nvm)/nvm.sh
	```
5. 最后让你的 shell 配置及时生效
	
	`source ~/.bash_profile`或`source ~/.zshrc`

	这样之后不会再出现关闭终端重启,或者重启机器发现 node ,npm 等系统环境变量失效的问题了.
	
	
**方法二:(推荐)**

CUrl方式安装

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.29.0/install.sh | bash
```
编辑 `$~/.zshrc`配置文件,写入下面这两行代码，保存后`source ~/.zshrc`
	
```
export NVM_DIR=~/.nvm
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm
```

## 使用nvm安装node.js


	用`$ nvm ls-remote`指令看一下有哪些版本可以安裝
	
	用`$ nvm install <version>`安装指定版本
	
	`$ nvm ls`查看安装的版本
	
	设置默认版本`$ nvm alias default <version>`　
	
## Npm Usage

	
	安装包:

	```
	$ npm install <package>     # 安装在本地项目中
	$ npm install -g <package>  # 安装在全局
	```
	推荐全局安装的包:
	
	```
	$ npm install -g coffee-script
	$ npm install -g grunt-cli
	```
	


	安装包，并且将其保存你项目中的 package.json 文件:
	`$ npm install <package> --save`

	查看 npm 安装的内容:

	```
	$ npm list     # 本地
	$ npm list -g  # 全局
	```

	查看过期的包（本地或全局）:`$ npm outdated [-g]`

	更新全部或特别指定一个包:`$ npm update [<package>]`

	卸载包:`$ npm uninstall <package>`
	
## 参考
	
[Node Version Manager](https://github.com/creationix/nvm)

[搭建 Node.js 开发环境](https://github.com/alsotang/node-lessons/tree/master/lesson0)

[node.js 版本控制 nvm 和 n 使用 及 nvm 重启终端失效的解决方法](http://yijiebuyi.com/blog/b1328ffe88cdde6b4102894635cf8f11.html)

[Node.js 安裝與版本切換教學 (for MAC)](http://icarus4.logdown.com/posts/175092-nodejs-installation-guide)


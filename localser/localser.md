## 本地服务器

基本上配置一个mac自带的本地apache服务器就足够前端开发用啦！我在配置本地服务器的时候遇到了不能访问<http://localhost/~username/>的问题。下面是我的解决过程。

启动Apache:`$ sudo apachectl start`

查看Apache版本:`$ httpd -v`

访问<http://localhost/~username/>,提示**Not Found**

**我们需要以下步骤:**

首先配置**username.conf**(需要管理员权限,`sudo`):
`/etc/apache2/users/username.conf`

将以下代码保存到**conf**文件中:
```
<Directory "/Users/yang/Sites/">
    Options Indexes MultiViews
    AllowOverride None
    Require all granted
</Directory>
```

给权限:`$ sudo chmod 755 /etc/apache2/users/username.conf`

启用几个支持:在`/etc/apache2/httpd.conf`中

查找并去掉代码行前边的#，启用如下:

```
LoadModule authz_core_module libexec/apache2/mod_authz_core.so
LoadModule authz_host_module libexec/apache2/mod_authz_host.so
LoadModule userdir_module libexec/apache2/mod_userdir.so
Include /private/etc/apache2/extra/httpd-userdir.conf
```

接着运行:`$ sudo nano /etc/apache2/extra/httpd-userdir.conf`

开启:`Include /private/etc/apache2/users/*.conf`

重启Apache:`$ sudo apachectl restart`

此时，就能进入<http://localhost/~username/>啦！

[Apache localhost/~username/ not working](http://stackoverflow.com/questions/24583859/apache-localhost-username-not-working/)

[Mac OS X Yosemite 10.10 配置 Apache+PHP 教程注意事项](http://yangjunwei.com/a/1568.html)

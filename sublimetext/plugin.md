## 插件

### 常用插件推荐

```
Emmet -> 代码缩写、补完
DocBlock -> 注释模版
SideBarEnhancementsn -> 侧边栏增强
ColorPicker -> 拾色器 cmd＋shift＋c
Bracket Highlighter -> 括号匹配提示
LiveReload -> 免刷新
ColorHighlighter -> css颜色代码显示颜色
LiveStyle -> css实时改变
JsFormat -> Js／JSON格式化 ctrl＋alt＋f

```

### LiveReload实时预览

**OSX users**安装

```
cd ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/

rm -rf LiveReload
git clone https://github.com/Grafikart/ST3-LiveReload.git LiveReload
```

[浏览器插件下载](http://livereload.com/extensions/)

chrome浏览器下需要配置liveReload插件:勾选**允许访问文件网址**

**在sublime text3 配置LiveReload**

方法一:

`preferences -> Packge Settings -> LiveReload -> Settings -> User`:


```
{
    "enabled_plugins": [
        "SimpleReloadPlugin",
        "SimpleRefresh"
    ]
}

```
方法二:

```
1. ctrl+shift+p
2. LiveReload: Enable/disable plugins
3. Enable - SimpleReload
```

### JsFormat格式化插件

* [JsFormat](http://www.icyfire.me/2014/10/28/sublime-text-plugin-jsformat.html)

	默认的快捷键为Ctrl + Alt + f

### SublimeLinter Settings


```
{
    "user": {
        "debug": false,
        "delay": 0.25,
        "error_color": "D02000",
        "gutter_theme": "none",
        "gutter_theme_excludes": [],
        "lint_mode": "background",
        "linters": {
            "pep8": {
                "@disable": false,
                "args": [],
                "disable": "",
                "enable": "",
                "excludes": [],
                "ignore": "",
                "max-line-length": null,
                "rcfile": "",
                "select": ""
            }
        },
        "mark_style": "outline",
        "no_column_highlights_line": false,
        "paths": {
            "linux": [],
            "osx": [
                "/usr/local/bin/"
            ],
            "windows": []
        },
        "python_paths": {
            "linux": [],
            "osx": [
                "/usr/local/bin/"
            ],
            "windows": []
        },
        "rc_search_limit": 3,
        "shell_timeout": 10,
        "show_errors_on_save": false,
        "show_marks_in_minimap": true,
        "syntax_map": {
            "html (django)": "html",
            "html (rails)": "html",
            "html 5": "html",
            "php": "html",
            "python django": "python"
        },
        "warning_color": "DDB700",
        "wrap_find": true
    }
}
```


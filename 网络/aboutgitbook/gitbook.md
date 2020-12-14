# Gitbook

GitBook 是一个基于 Node.js 的命令行工具，可使用 Github/Git 和 Markdown 来制作精美的电子书，GitBook 并非关于 Git 的教程。

GitBook 是一个基于 Node.js 的命令行工具，可使用 Github/Git 和 Markdown 来制作精美的电子书，GitBook 并非关于 Git 的教程。

**GitBook支持输出多种文档格式：**

* 静态站点：GitBook默认输出该种格式，生成的静态站点可直接托管搭载Github Pages服务上。
* PDF：需要安装gitbook-pdf依赖。
* eBook：需要安装ebook-convert。
* 单HTML网页：支持将内容输出为单页的HTML，不过一般用在将电子书格式转换为PDF或eBook的中间过程。
* JSON：一般用于电子书的调试或元数据提取。

使用GitBook制作电子书，必备两个文件：README.md和SUMMARY.md。

**本网站就是用 Gitbook 制作的**

<hr>

## 一、安装：

> **info**
>
> **提示：** 安装 gitbook 之前要先安装 node.js，因为兼容性问题，下载老版本node.js：https://nodejs.org/en/blog/release/v12.13.0/

​	安装node后，在 cmd 里 运行该语句，安装gitbook到本地：

```js
$ npm install gitbook-cli -g
```

## 二、使用：

**1. 新建书籍：**进入想要存放书籍的文件夹，运行该语句：

```
$ gitbook init
```

**2. 预览书籍：**运行该语句，并打开生成的ip地址预览书籍：

```
$ gitbook serve
```

**3. 发布书籍：**运行该语句，构建发布：

```
$ gitbook build
```

**4. 生成电子书：**(第一次生成时，根据提示安装插件)

```
$ gitbook pdf
$ gitbook epub
$ gitbook mobi
```

## 三、配置：

### 1、book.json配置文件：

**gitbook**

`{ "description": "This is such a great book!" }`

**description**

`{ "description": "This is such a great book!" }`

**styles**

这个选项是用来自定义书本的css的。

例子：

```json
{
    "styles": {
        "website": "styles/website.css",
        "ebook": "styles/ebook.css",
        "pdf": "styles/pdf.css",
        "mobi": "styles/mobi.css",
        "epub": "styles/epub.css"
    }
}
```

**plugins**

```json
{ "plugins": ["mathjax"] }
```

书本使用的插件列表被定义在 `book.json` 的配置中。

**pluginsConfig**

```json
{
    "plugins": ["myplugin"],
    "pluginsConfig": {
        "myPlugin": {
            "message": "Hello World"
        }
    }
}
```

**structure**

这个选项是用来覆盖GitBook使用的路径的。

例如你想要使用 `INTRO.md` 代替 `README.md`：

```json
{
    "structure": {
        "readme": "INTRO.md"
    }
}
```

**variables**

```json
{
    "variables": {
        "myTest": "Hello World"
    }
}
```

<hr>

### 2、我的 book.json：

```json
{
    "name": "Yesura",
    "version": "0.0.0",
    "description": "Yesura",
    "main": "./index.js",
    "gitbook": "^3.2.3",
    "gitbook-cli": "^2.3.2",
    


    "root": "./content",
    "output": "./docs",
    "title": "Yesura",
    "plugins": [
      "-lunr", "-search", "search-pro",
      "fontsettings", 
      "-highlight", "prism", "prism-themes",
      "styled-blockquotes",
      "copy-code-button",
      "cuav-chapters",
      "anchor-navigation-ex-toc"
    ],
    "pluginsConfig": {
      "prism": {
          "css": ["prismjs/themes/prism-okaidia.css"]
       },
       "anchor-navigation-ex-toc": {
        "showLevel": false
       }
    },
    
    
    "styles": {
      "website": "styles/website.css",
      "ebook": "styles/ebook.css",
      "pdf": "styles/pdf.css",
      "mobi": "styles/mobi.css",
      "epub": "styles/epub.css"
    },
    

    
    "variables": {
        "version": "1.0.0"
    }
}  
```

### 3、去掉自带链接：“[Published with GitBook](https://www.gitbook.com/)”

	找到summary.html，屏蔽链接：

```
C:\Users\.gitbook\versions\3.2.3\node_modules\gitbook-plugin-theme-default\_layouts\website\summary.html
```
## 四、插件：
### 1、搜索：

​	去npm官网搜索gitbook插件：https://www.npmjs.com/

### 2、我安装的插件：

1. 中文搜索：https://www.npmjs.com/package/gitbook-plugin-search-pro-fixed
2. 代码高亮：https://www.npmjs.com/package/gitbook-plugin-prism-dw
3. 引用模块：https://www.npmjs.com/package/gitbook-plugin-styled-blockquotes
4. 生成目录：https://www.npmjs.com/package/gitbook-plugin-anchor-navigation-ex-toc

### 3、安装与禁用

​	在 book.json 文件里配置插件，插件名前加 “-” 意思是禁用该插件。

```json
{
   "plugins": ["-highlight", "prism", "prism-themes"]
}
"pluginsConfig": {
  "prism": {
    "css": [
      "prismjs/themes/prism-solarizedlight.css"
    ]
  }
}
```

​	配置好以后，运行安装命令：

```
$ gitbook install
```


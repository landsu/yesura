# Gitbook

GitBook 是一个基于 Node.js 的命令行工具，可使用 Github/Git 和 Markdown 来制作精美的电子书，GitBook 并非关于 Git 的教程。

GitBook 是一个基于 Node.js 的命令行工具，可使用 Github/Git 和 Markdown 来制作精美的电子书，GitBook 并非关于 Git 的教程。

##### GitBook支持输出多种文档格式：
* 静态站点：GitBook默认输出该种格式，生成的静态站点可直接托管搭载Github Pages服务上。
* PDF：需要安装gitbook-pdf依赖。
* eBook：需要安装ebook-convert。
* 单HTML网页：支持将内容输出为单页的HTML，不过一般用在将电子书格式转换为PDF或eBook的中间过程。
* JSON：一般用于电子书的调试或元数据提取。

使用GitBook制作电子书，必备两个文件：README.md和SUMMARY.md。

##### 本网站就是用 Gitbook 制作的

<hr>

### 安装与使用：

#### 一、安装：

> **info**
>
> **提示：** 安装 gitbook 之前要先安装 node.js，因为兼容性问题，下载老版本node.js：https://nodejs.org/en/blog/release/v12.13.0/

​	安装node后，在 cmd 里 运行该语句，安装gitbook到本地：

```
$ npm install gitbook-cli -g
```

#### 二、使用：

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
# CHM 制作与反编译

## 一、CHM 制作：

###  1、工具：Microsoft Html Help Workshop

- 免费、功能齐全
- 搜索本地电脑：“Html Help Workshop”，若没有集成在系统里，网络搜索，下载安装。

###  2、使用说明：

![](..\..\pic\001 chm\001chm001.jpg)

- 1 — 工程属性：

  - 勾选 “Compile full-text search information” (开启全文搜索)

    ![](..\..\pic\001 chm\2020-12-07_19-03205.jpg)

- 2 — 添加页面：

  - 若是已经做好各个页面的链接，像一个网站一样，只添加首页即可

- 3 — 自定义窗口设置：

  - Buttons 定义窗口按钮：
  - Navigation Pane: 勾选 Search tab 和 Advanced  (搜索页，高级搜索)
    - 在设置好后点击 “确定” 按钮时，会有一个勾选 “Compile full-text search information” 的选项，勾选它
    - 勾选后，效果是和 “1— 工程属性” 设置是一样的。
  - Files：
    - TOC：目录文件
    - Index: 索引文件
    - Default: 打开文档时，默认显示页
    - Home：首页
    - Jump 1&2: 自定义链接（需勾选 “Buttons” 里面的 Jump 按钮）	![](..\..\pic\001 chm\2020-12-07_18-55796.jpg)

- 4 — 编译

- Contents — 设置目录结构：

  - 1 — 父级文件（需要关联页面）
  - 2 — 子级文件（需要关联页面）
  - 3 — 编辑页面
  - 4 — 删除页面
  - 5 — 移动页面

  ![](..\..\pic\001 chm\2020-12-07_19-09088.jpg)

- Index — 关键字索引（像电子词典）

  - 1 — 添加关键字 
    - 每个关键字，都可以链接多个页面
  - 2 — 按字母表排序所有关键字

  ![](..\..\pic\001 chm\2020-12-07_19-16690.jpg)

## 二、成品效果：

![](..\..\pic\001 chm\2020-12-07_19-26428.jpg)

## 三、CHM 反编译：

​	在chm所在文件夹运行 ***Windows Powershell***：

```powershell
hh.exe -decompile ./ C:\Users\Me\Desktop\123.chm
```

****

**注释：** 

- “hh.exe” — Html Help.exe
- “-decompile” — 反编译
- “./ ” — 输出到源文件夹，也可以设置为其他文件夹
- “C:\Users\Me\Desktop\123.chm” — 需要反编译的文件

**反编译之后，就可以得到该chm文档的源文件，编译速度、质量都不会比收费软件差**
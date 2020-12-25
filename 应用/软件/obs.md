# OBS 多平台直播

> **info** 尽量用配置高的电脑进行直播



## 一、OBS下载与安装: 

### 1、软件安装： [下载](https://obsproject.com/)

### 2、默认安装即可



## 二、OBS 使用教学：

> **info** 	Youtube 搜索 “OBS教学”，来学习如何使用



## 三、多平台

### 1、Youtube：

* OBS 文件 》 设置 》 推流 》选择 Youtube 》输入Youtube 的直播密钥即可
* 这个是主直播平台，其他平台可以用 OBS “直播多开插件”

### 2、Facebook, IG, 任何其他支持PTMP的平台:

* [直播多开插件](https://github.com/sorayuki/obs-multi-rtmp/releases/)
  * 下载后解压
  * 关闭OBS软件
  * 复制解压内容到OBS根目录，默认路径：C:\Program Files\obs-studio
* OBS主界面左侧多出 “多路推流”，点击 “新建推流目标”，逐个设置 Facebook、IG等平台
* 获取 IG 的 RTMP URL 和 Stream key
  * [Yellow Duck](https://yellowduck.tv/) (下载、安装)
  * 安装后，登陆IG账号，即可获得
* 左侧列表可以点击 “开始” 或 “停止” 来控制各平台的直播

### 3、Line聊天室直播

* [虚拟摄像头](https://obsproject.com/forum/resources/obs-virtualcam.539/)（Line群组直播）
  * 下载直接默认安装
  * OBS 工具 》 虚拟摄像头 》 开启
* 用电脑 Line 发起直播，Line 直播设置里，视频选择 OBS-Camera 虚拟摄像头即可

### 4、网站平台

* 进入 Youtube 直播账号的视频列表，找到直播视频，右键复制视频地址，或嵌入代码
* 然后粘贴代码到网站的帖子里，嵌入Youtube直播即可

## 四、界面：

- 左侧 “多路推流” 列表，点击开始按钮既开始直播
- 下方 “来源” 是捕捉视频来源，可以是整个屏幕，可以是某个窗口，可以是浏览器等等，也可以混合多种元素
- 右下角 “控件”，点击 “开始推流”，即可开始主直播平台的直播，主直播平台设置参三1

![](..\..\pic\002 obs\1.jpg)


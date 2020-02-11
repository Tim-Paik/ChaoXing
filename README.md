# ChaoXing

#### 介绍
非官方版超星学习通win客户端，使用nativefier进行打包

#### 软件架构
使用了nativefier进行打包，应用程序由Electron包装在操作系统可执行文件中。
[nativefier项目地址](https://github.com/jiahaog/nativefier)
使用Inno Setup进行安装包制作。

#### 如何使用安装

1. 前往[releases](https://gitee.com/timpaik/ChaoXing/releases)页面下载最新的exe安装包
2. 双击安装包，下一步
3. 安装完成！

#### 使用说明
请在1280×720分辨率以上的屏幕中使用，否则可能显示不全

#### 免责条款

本网站内容来自i.chaoxinng.com，内容真实性、准确性、合法性由网站所有者负责。
如有侵权请联系timpaik@163.com
本软件仅为研究学习之用，请勿商业盈利传播。
任何单位或个人使用本软件从事商业营利活动，请自行承担相应的法律责任。详细请参照 超星学习通官网的相关条款。
任何因使用本软件导致的损失，无论是BUG或错误使用而导致的错误，本人均不承担任何责任。
如对此免责条款有疑问或反对，请勿安装。

#### 使用nativefier参数
您可以在完整安装了nativefier的前提下在Windows命令提示符中使用以下命令进行打包：
```
nativefier -n "ChaoXing" "i.chaoxing.com" --flash --single-instance --zoom 0.89 --width 1280  --height 720 --min-width 1280 --min-height 720 --honest --insecure --disable-dev-tools --disable-context-menu -i "favicon.ico"
```
会生成一个名为ChaoXing-win32-x64的文件夹
Linux&macOS同理，参见[nativefier](https://github.com/jiahaog/nativefier)
打包后可用Inno Setup进行安装包制作，下载ChaoXing.iss后将打包好的ChaoXing-win32-x64文件夹改名为ChaoXing并复制到"C:\Program Files\"，然后右键ChaoXing.iss编译即可，会输出到C盘根目录。
##### 使用时请注意：要将"favicon.ico"复制到命令提示符的当前目录中，此favicon.ico为本人制作


### 更新日志
#### 0.1.1
置换了高清图标，详见".\icons\"中的文件。
#### 0.1.0
支持flash，模拟chromium内核，兼容性好些了
理论上支持直播录播（但由于服务器卡顿没有老师直播无法测试，不能用的话我也没辙）
搞了个安装包，可以创建开始菜单文件夹和快捷方式了
修改了最小窗口大小，防止显示不全的情况
添加了免责条款
禁用了上下文菜单，添加了正经的软件图标，禁用了chrome开发者工具
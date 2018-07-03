# 学习macOS

## 快捷键
* 系统
Command+I     显示选中的文件的“显示简介”窗口
Command+W     关闭当前应用的窗口
Command+Q     退出当前应用程序（和command+tab配合可快速批量关闭应用程序）
Command+Delete     移到废纸篓
Command+Shift+Delete     清倒废纸蒌，需要确认。
Command+Option+Shift+Delete     清倒废纸蒌，不需要确认。
Command+C     复制
Command+V     粘贴
Command+Option+V     移动（剪切）
Command+Option+D     显示或隐藏 Dock
Command+Control+F     当前窗口全屏
Command+H     当前窗口隐藏
Command+M     当前窗口最小化
Control+Shift+Power     关闭屏幕
Control+F2     将焦点移到菜单栏
打开｜关闭勿扰模式     按住 Option ，单击 屏幕右上角。

* 功能键
F11     隐藏｜打开 所有打开的窗口（回到桌面）
Fn+F3     Command-Mission Control (F3)     显示桌面
Fn+F4     Launchpad

* 拍摄屏幕快照
Command+Shift+3     将屏幕捕捉到**文件**
Command+Shift+4     将所选屏幕内容捕捉到**文件**，或按空格键仅捕捉一个窗口
Command-Shift-Control-3     将屏幕内容捕捉到**剪贴板**
Command-Shift-Control-4     将所选屏幕内容捕捉到**剪贴板**，或按空格键仅捕捉一个窗口

## 常用命令
* 查找指定目录下（包含子目录）所有的指定名字的文件，可以使用通配符（? *）
```shell
$ find . -name '.DS_Store'
$ find . -name '.DS_*'
$ find . -name '.DS_Stor?'

./.DS_Store
./test/.DS_Store
./images/.DS_Store
```

* 删除指定目录下（包含子目录）所有的指定名字的文件
```shell
$ find . -name '.DS_Store' -delete
```

* 批量处理图片
```shell
$ sips -Z 400 *.png     宽度400 高度按等比进行处理
$ sips -z 800 1200 *.png     高度800，宽度1200
$ sips -z 800 1200 *.png —out dir     输出到指定目录
```

* 显示磁盘使用统计信息
```shell
$ du -sh
 23M    .

$ du -sh *
 22M    2017-11
1.0M    2017-12
336K    2018-01
152K    rz
 24K    x.docx
 28K    y.xlsx
```

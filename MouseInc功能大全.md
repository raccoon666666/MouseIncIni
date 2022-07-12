### 功能

#### 自身类

##### 开关

| 代码                                 | 作用                |
| ------------------------------------ | ------------------- |
| ["Internal", "Settings"]             | 设置界面            |
| ["Internal", "Exit"]                 | 退出                |
| ["Internal", "Pause"]                | 暂停 / 恢复功能     |
| ["Internal", "Icon"]                 | 隐藏 / 恢复托盘图标 |
| ["Internal", "Reload"]               | 加载配置文件        |
| ["Internal", "Config", "k1.k2", "v"] | 修改配置文件        |

##### 手动功能

| 代码                                    | 作用        |
| --------------------------------------- | ----------- |
| ["Internal", "ClipboardMenu"]           | Ctrl+cc菜单 |
| ["Internal", "Exclude"]                 | 排除当前    |
| ["Internal", "Print", "str"]            | 打印信息    |
| ["Internal", "ShowTips", "s1",...,"sn"] | 右下提示    |



#### 窗口类

##### 窗口

| 代码                       | 作用                |
| -------------------------- | ------------------- |
| ["Window", "Minimize"]     | 最小化              |
| ["Window", "Maximize"]     | 最大化              |
| ["Window", "Close"]        | 关闭                |
| ["Window", "CloseSimilar"] | 关闭同类            |
| ["Window", "HideTray"]     | 最小化到托盘        |
| ["Window", "ShowTray"]     | 恢复所有托盘        |
| ["Window", "ToggleTray"]   | 隐藏到 / 恢复出托盘 |
| ["Window", "Top"]          | 固定                |
| ["Window", "Center"]       | 居中                |
| ["Activate"]               | 激活                |



##### 截图

> `Ctrl+C` 复制到剪贴板
> `Ctrl+S` 保存该贴图
> `Ctrl+O` OCR识别
> `Ctrl+W` 关闭贴图

| 代码                                 | 作用     | 备注                                                         |
| ------------------------------------ | -------- | ------------------------------------------------------------ |
| ["Screenshot", "参数"]               | 手势截图 | ToClipboard`,`ToFile`,`Stick`,`PiP`,`OCR                     |
| ["Snapshot", "参数"]                 | 矩形截图 | ToClipboard`,`ToFile`,`Stick`,`PiP`,`OCR                     |
| ["ScreenshotHQ", "参数", "arg\|arg"] | 窗口截图 | DrawCursor 绘制鼠标指针<br>TransparencyGrid 使用透明网格填充背景 |



##### 显示器

| 代码                           | 作用       |
| ------------------------------ | ---------- |
| ["Explorer", "turnoffmonitor"] | 关闭显示器 |
| ["SetBrightness", "UP"]        | 增大亮度   |
| ["SetBrightness", "DOWN"]      | 降低亮度   |
| ["SetBrightness", "DEFAULT"]   | 默认亮度   |



#### 按键类

##### 按键

> `["SendKeys", "A"]`   完整按下
>
> > `["SendKeys", "A", "NOACTIVATE"] 不激活窗口`
>
> `["SendKeyDown", "A"]`  按下
>
> `["SendKeyUp", "A"]`  松开

| 特殊按键                             | 备注          |
| ------------------------------------ | ------------- |
| Escape                               | Esc键         |
| PrtSc                                | 截图键        |
| Scroll                               | 页面滚动      |
| Pause                                | 暂停print     |
| Break                                | 中断exe       |
| Del                                  | Delete / 句点 |
| Left, Right, Up, Down                | ↑ ↓ ← →       |
| PageUp, PageDown, PgUp, PgDn         | 翻页          |
| Plus, Minus                          | + -           |
| Back, Forward, Refresh               | 浏览器按键    |
| VolumeMute, VolumeDown, VolumeUp     | 音量按键      |
| MediaNext, MediaPrev, MediaPlayPause | 多媒体按键    |
| Num 0 - Num 9                        | 小键盘        |



##### 鼠标

| 代码                    | 作用 | 备注                  |
| ----------------------- | ---- | --------------------- |
| ["SendClick", "left"]   | 按键 | left`,`right`,`middle |
| ["MouseMove", "x", "y"] | 移动 |                       |



#### 系统类

##### 变量

| 变量      | 作用                   |
| --------- | ---------------------- |
| appdir    | MouseInc安装目录       |
| port      | MouseInc设置界面的端口 |
| clipboard | 剪贴板内容             |
| filepath  | 窗口进程.所在路径      |
| filename  | 窗口进程.名            |
| pid       | 窗口进程.PID           |



##### 系统

| 代码           | 作用           | 备注          |
| - | - | - |
| ["Execute", "notepad 1.txt","额外参数"] | Ctrl+R执行  | hide`,`admin`,`wait  |
| ["Execute2", "文件"]     | Explorer执行   |         |
| ["Internal", "Delay", "1000"] | Sleep | |
| ["PostMessage", "272", "40022"] | 向窗口发消息 | 参数: WM_SYSCOMMAND, <br>IDC_MANAGE_EXTENSIONS, 默认0 |
| ["RegSet", "位置", "HideFileExt", "0"] | 设置注册表 | 只支持数字和字符串 |



##### 文件

| 代码                                   | 作用       | 备注 |
| -------------------------------------- | ---------- | ---- |
| ["Explorer", "select", "路径"]         | 打开路径   |      |
| ["Explorer", "recyclebin", "arg\|arg"] | 清空回收站 | noconfirmation无需确认<br>noprogressui不显示进度 |



#### 数据类

##### 剪贴板

| 代码                     | 作用           | 备注                 |
| ------------------------ | -------------- | -------------------- |
| ["SetClipboard", "text"] | 写入剪贴板     | 转义"和\             |
| ["GetClipboard", "参数"] | 读取剪贴板图片 | Stick`,`ToFile`,`OCR |



##### 编解码

| 代码                              | 作用       |
| --------------------------------- | ---------- |
| ["Algorithm", "b64decode", "Str"] | base64解码 |
| ["Algorithm", "b64encode", "Str"] | base64编码 |
| ["Algorithm", "urldncode", "Str"] | URL解码    |
| ["Algorithm", "urlencode", "Str"] | URL编码    |
| ["Algorithm", "md5", "Str"]       | MD5摘要    |
| ["Algorithm", "sha1", "Str"]      | SHA1摘要   |
| ["Algorithm", "sha256", "Str"]    | SHA256摘要 |
| ["Algorithm", "qrcode", Str"]     | 二维码     |
| ["Algorithm", "CyberChef", "Str"] | 智能检测   |




ctrl+prtSc截图



边缘滚动
右键滚轮
Ctrl+CC


M：打开设置窗口
Z：屏蔽当前程序



window  //  窗口控制

        maximize	最大化
        minimize	最小化
        top		置顶
        center	居中
        close		关闭窗口
        closesimilar	关闭同程序窗口
        hidetray	托盘隐藏
        toggletray	托盘显隐
        showtray	托盘显示

internal  //  自身

        settings	设置窗口
        exit		退出
        pause		暂停
        icon		托盘显隐
        ClipboardMenu	增强粘贴
        exclude		排除程序
        reload		加载配置
        config		修改配置		["Internal", "Config", "ShowTrayIcon", "false"]
        delay		延时(毫秒)		["Internal", "Delay", "1000"]
        showtips	提示信息		["Internal", "ShowTips", ("标题"),("内容")]

sendkeys  //  模拟按键

        Escape        Esc        Tab        Backspace        Enter        Space
        PrtSc        Scroll        Pause        Break        Insert        Delete
        Del        Home        End        Left        Right        Up        Down
        PageUp        PageDown        PgUp        PgDn        Plus        Minus
        浏览器 Back, Forward, Refresh
        音量 VolumeMute, VolumeDown, VolumeUp
       多媒体 MediaNext, MediaPrev, MediaPlayPause
        小键盘 'Num 0 - Num 9'   

sendkeydown  //  模拟按下
        ["SendKeyDown", "Ctrl"]

sendkeyup  //  模拟松开
        ["SendKeyUp", "Ctrl"]

sendclick  //  模拟点击
        left        right        middle

mousemove  //  模拟鼠标放置
        ["MouseMove", "100", "300"]

SetClipboard  //  设置剪贴板
        ["SetClipboard", "text"]

execute  //  命令行&网页
        ["Execute", "命令"]
        ["Execute", "https://www.baidu.com/"]  
       	 	%appdir%	MouscInc所在目录
        	%clipboard%	剪贴板文字内容
        	%filepath%	激活窗口进程路径
        	%filename%	激活窗口进程名称
        	%pid%	激活窗口进程id
        	%port%	MouseInc设置端口
	！！注意转义

Screenshot  //  全窗口截图
ScreenshotHQ  //  全窗口高级截图
        ["ScreenshotHQ", "ToFile", "DrawCursor|TransparencyGrid"]
Snapshot  //  自定义窗口截图
GetClipboard  //  从剪贴板
        ["Screenshot", "ToClipboard"]  //  到剪贴板
        ["Screenshot", "ToFile"]  //  到文件
        ["Screenshot", "Stick"]  //  到浮窗
                拖动窗口：左键
                退出：Esc  &  右键
                调整大小：边缘
                透明度：滚轮
                还原：双击  &  空格  &  回车
                Ctrl+C 复制到剪贴板
                Ctrl+S 保存该贴图
                Ctrl+O OCR识别
                Ctrl+W 关闭贴图
                使用w,a,s,d每次可移动10个像素。
                使用↑,←,↓,→每次可移动1个像素
        ["Screenshot", "PiP"]  //  画中画
                拖动窗口：左键
                退出：Esc  &  右键
                调整大小：边缘
                透明度：滚轮
                还原：双击  &  空格  &  回车
                使用w,a,s,d每次可移动10个像素。
                使用↑,←,↓,→每次可移动1个像素
        ["Screenshot", "OCR"]  //  转文字

Algorithm  //  编码算法
        ["Algorithm", "b64decode", "%clipboard%"]  //  base64解码
        ["Algorithm", "b64encode", "%clipboard%"]  //  base64编码
        ["Algorithm", "urlencode", "%clipboard%"]  //  url编码
        ["Algorithm", "urldecode", "%clipboard%"]  //  url解码
        ["Algorithm", "md5", "%clipboard%"]  //  md5编码
        ["Algorithm", "sha1", "%clipboard%"]  //  sha1编码
        ["Algorithm", "sha256", "%clipboard%"]  //  sha256编码
        ["Algorithm", "CyberChef", "%clipboard%"]  //  自动
        ["Algorithm", "qrcode", "%clipboard%"]  //  二维码

Explorer  //  文件操作
        ["Explorer", "select", "%fullpath%"]  //  打开文件夹位置
        ["Explorer", "recyclebin", "noconfirmation|noprogressui"]  //  清空回收站
        ["Explorer", "turnoffmonitor"]  //  关闭屏幕

SetBrightness  //  亮度调节
        ["SetBrightness", "UP"]
        ["SetBrightness", "DOWN"]
        ["SetBrightness", "DEFAULT"]

RegSet  //  注册表操作








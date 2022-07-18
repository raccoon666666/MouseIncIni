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






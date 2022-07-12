##### Action序列

```json
Actions:[A,A,A]
Action:["动作名","参数",...,"参数"]
```

##### 配置文件结构

> AltDrag : 是否${\color{Red}快速移动窗口}$(按住Alt拖动)
>
> WheelAltControl : 是否${\color{Red}快速音量调节}$(Alt滚轮调节音量)
>
> VolumeControlSound : 是否${\color{Red}音量反馈}$(音量调节时播放音效)
>
> VolumeSoundIndex : ${\color{Red}音量反馈音效}$(0清脆、1泡泡音)
>
> KeySound : 是否${\color{Red}按键音效}$
>
> KeySoundIndex : ${\color{Red}按键音效}$(0打字机、1青轴、2茶轴、3红轴、4G轴)
>
> IgnoreFullScreen : 是否${\color{Red}全屏时暂停使用}$
>
> ShowTrayIcon : 是否${\color{Red}在托盘显示图标}$
>
> 
>
> CapsLockLed : 是否${\color{Red}显示大写锁定}$
>
> CapsUnlock : 是否${\color{Red}关闭大写锁定}$(30s后)
>
> WheelThrough : 是否${\color{Red}滚轮穿透}$
>
> WheelNatural : 是否${\color{Red}滚轮反向}$
>
> AutoClip : 是否${\color{Red}快速复制}$(选中后自动复制)
>
> FastPaste : 是否${\color{Red}快速粘贴}$(按住左键后右键)
>
> Administrator : 是否${\color{Red}管理员权限}$
>
> 
>
> Excludes${\color{Red}排除程序序列}$
>
> > []
>
> 
>
> MouseGesture  ${\color{Red}鼠标手势}$
>
> > Open : 是否开启
> >
> > WheelSwitch: 是否开启`右键滚轮`
> >
> > AddMode : 是否开启添加模式
> >
> > DrawColor : "#rrggbb手势颜色"
> >
> > RandColor : 是否开启随机颜色
> >
> > DrawTrace : 是否显示轨迹
> >
> > TraceArrow : 是否开启轨迹箭头
> >
> > TraceWidth : 轨迹宽度
> >
> > DrawResult : 显示提示
> >
> > FontSize : 文字大小
> >
> > Offset : 文字位置
> >
> > FailColor : "#rrggbb添加失败颜色"
> >
> > StartDistance : 触发距离(移动至少pixel才触发)
> >
> > Timeout : 停顿超时(超过ms中断该手势)
> >
> > RestoreEvent : 是否还原事件(手势失效却触发右键点击)
> >
> > Sensitive : 灵敏度
>
> 
>
> Gestures[]  ${\color{Red}手势大全}$
>
> > Sign : "手势名"	$\color{red}包括两个特殊的内置手势名:$`WheelSwitchUp 和 WheelSwitchDown`
> >
> > Data[]	`[x0,y0,...,xn,yn]`
>
> 
>
> MatchGlobal[]  ${\color{Red}全局软件手势配置}$
>
> > Valid : 是否开启
> >
> > Sign : "匹配的手势名"
> >
> > Name : "项名"
> >
> > Actions[]	`Action序列`
> >
>
> 
>
> MatchCustom[]  ${\color{Red}特定软件组手势配置}$
>
> > Name : "分组名"
> >
> > IgnoreGlobal : 是否屏蔽全局手势
> >
> > Match[]	$程序组匹配的程序$
> > 
> > List[]	`组内手势配置`
> > 
> > > Valid : 是否开启
> > >
> > > Sign : "匹配的手势名"
> > >
> > > Name : "项名"
> > >
> > > Actions[]	`Action序列`
> > >
>
> 
>
> WheelEdge  ${\color{Red}边缘滚动}$
>
> > Open : 是否开启
> >
> > Bottom	`Left、Right、Top`
> >
> > > Valid : 是否有效
> > >
> > > Name : "名称"
> > >
> > > UpActions[]	`向上滚动Action序列`
> > >
> > > DownActions[]	`向下滚动Action序列`
> > >
> > > PressActions[]	`鼠标中键Action序列`
> > >
>
> 
>
> HotCorner  ${\color{Red}触发角}$
>
> > Open : 是否开启
> >
> > BottomLeft		`BottomRight、TopLeft、TopRight`
> >
> > > Actions[]	`Action序列`
> > >
> > > Name : "项名"
> > >
> > > Valid : 是否开启
>
> 
>
> ClipboardManager  ${\color{Red}Ctrl+cc列表}$
>
> > Open : 是否开启
> >
> > Menu[]	`列表项序列`
> >
> > > Valid : 是否开启
> > >
> > > Name : "项名"		`使用&K表示快捷键`、`Name为空则表示分割线`
> > >
> > > Actions[]	`Action序列`		`Actions为空则表示二级菜单`
> > >
>
> 
>
> Hotkeys[]  ${\color{Red}全局热键大全}$
>
> > Valid : 是否开启
> >
> > Name : "项名"
> >
> > Key : "热键"
> >
> > Actions[]	`Action序列`
> >
>
> 
>
> Keycast  ${\color{Red}按键回显}$
>
> > Open : 是否开启
> >
> > IgnoreSingle : 是否忽略单字符
> >
> > BackgroundColor : "#rrggbb背景颜色"
> >
> > TextShadowColor : "#rrggbb阴影颜色"
> >
> > TextColor : "#rrggbb文字颜色"
> >
> > FontSize : 文字大小
> >
> > X : 显示窗口X偏移
> >
> > Y : 显示窗口Y偏移
> >
> > Space : 间距
> >
> > Fade : 消失秒数
>
> 
>
> Language : "语言选择"		`auto`
>
> Locales ${\color{Red}语言配置}$
>
> > en-US		`语言包zh-CN、zh-TW`
> >
> > > key : value
>


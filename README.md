# EFI-B360m_d2v_OpenCore_dvi_uhd630
OC引导工具 EFI 配置文件

Open Core版本: 0.5.6 beta 2020/2/24 详情: [Open Core 最新自动编译版](https://github.com/williambj1/OpenCore-Factory)、[Open Core 官方版](https://github.com/acidanthera/OpenCorePkg/releases)

Clover引导文件请看这里：[Clover引导](https://github.com/Matchas-xiaobin/EFI-B360m_d2v_dvi_uhd630)

# 参考资料
很多教程和系统下载: [黑果小兵的部落阁](https://blog.daliansky.net/)

XJN大佬的OC教程: [使用OpenCore引导黑苹果](https://blog.xjn819.com/?p=543)

黑果小兵的OC教程: [精解OpenCore](https://blog.daliansky.net/OpenCore-BootLoader.html)

# 机器配置
```
CPU: intel i5-8400
内存: 16G
显卡: UHD630

[GIGABYTE B360m d2v 主板官网](https://www.gigabyte.cn/Motherboard/B360M-D2V-rev-10/sp#sp)
主板: GIGABYTE B360m d2v
声卡: Realtek ALC887
网卡: Realtek 8118

注意自行修改EFI中机型信息
```

# 更新记录

### 2020.2.27 系统版本 10.15.3
```
1. 解锁CFG Lock;
请务必解锁CFG在使用这个EFI配置, 如果不解锁CFG或者不会, 请修改config.plist如下配置内容:
Kernel—–Quirks: AppleCpuPmCfgLock - yes/true
Kernel—–Quirks: AppleXcpmCfgLock - yes/true
UEFI—-Quirks: IgnoreInvalidFlexRatio - yes/true
(危!)没有解锁CFG并且没有修改这几个参数, 将会无法引导系统。
解锁方式可以参考CFG Lock文件夹下的相关文档以及使用 'baidu'、'google' 等搜索引擎进行搜索
2. 修改缓冲帧信息, 核显不在识别为移动端。
```

### 2020.2.24 系统版本 10.15.3
```
1. 升级OC版本到0.5.6;
2. 启动转换助理貌似可以用了, 没测试, 但是之前打开后点继续是发生内部错误;
3. 注意自行修改EFI中机型信息;
```

### 2020.2.11 系统版本 10.15.3
```
1. 去掉一些没用的重命名patch;
2. 加入强制睡眠aml，尝试修复10.15.2开始出现的无法睡眠的问题;
```

### 2020.2.10 系统版本 10.15.3
```
1. 更新到最新发布版本 OC 0.5.5 正式版;
2. 更换声卡ID到40（原先11），现在开机默认是 线路输出;
3. OC 0.5.5 支持300系列主板原生NVRAM了，如果之前有模拟NVRAM，请删掉，详细参考XJN大佬教程 3.12 章节;
```

### 2019.12.6 系统版本 10.15.1
```
1. 更新缓冲帧信息，限制视频端口为2个，解决开机到登陆界面鼠标键盘卡顿的问题。目前还是会有3秒左右小卡顿，已经没啥影响了;
2. 屏蔽核显的数字音频功能，解决唤醒后重启的问题(不太确定, 暂时测试是没问题.);
3. 机型更换成 Macmini8,1 (所以如果之前用了我的EFI, 更新这个后, 机型会变, 需要重新登录Apple ID);
4. 升级OC版本为 0.5.3 正式版;
5. RTC重命名为ARTC(应该是没啥意义和实际作用, 白苹果强迫症);
```

# 目前使用体验
```
1. 核显DVI输出，显存1536M ---11月30号更新缓冲帧信息，显存2048M
2. 声卡ID 40 ---2月24号更改为 40 前面板 选 耳机，后面板 选 线路输出
3. 有线网卡 正常
4. USB 3.0 2.0 正常 （如果不正常，请定制USB）
5. 睡眠正常
6. 唤醒正常 ---12月6日 修复AppleALC导致唤醒重启的问题
7. 关机正常
8. 无花屏现象
```

# 目前碰到问题
```
1. 开机读条到4分之3左右会黑屏大约1~2秒，然后进入用户登录界面（好像只有核显都会有这毛病？）。
2. USB定制端口可能会出现问题，原因应该是不同机箱前置面板的USB端口可能不一样，定制USB可解决该问题。
```

# EFI-B360m_d2v_OpenCore_uhd630
OC引导工具 EFI 配置文件

Open Core版本: 0.5.9 2020/6/5 详情: [Open Core 最新自动编译版](https://github.com/williambj1/OpenCore-Factory)、[Open Core 官方版](https://github.com/acidanthera/OpenCorePkg/releases)

# 参考资料
很多教程和系统下载: [黑果小兵的部落阁](https://blog.daliansky.net/)

XJN大佬的OC教程: [使用OpenCore引导黑苹果](https://blog.xjn819.com/?p=543)

黑果小兵的OC教程: [精解OpenCore](https://blog.daliansky.net/OpenCore-BootLoader.html)

# 机器配置
```
CPU: intel i5-8400
内存: 16G
显卡: uhd630

[GIGABYTE B360m d2v 主板官网](https://www.gigabyte.cn/Motherboard/B360M-D2V-rev-10/sp#sp)
主板: GIGABYTE B360m d2v
声卡: Realtek ALC887
网卡: Realtek 8118

注意自行修改EFI中机型信息
```

# 说明
```
1. 机型为iMac19,2 解决开机鼠标, 键盘会卡顿的现象。
2. 核显DVI-I输出在10.15.5系统上，实测无法显示，VGA接口正常，所以要核显组双屏的，不要升级10.15.5。
3. 添加宪武大大的 '添加缺失的部件' 补丁。
```

# 目前使用体验
```
1. 核显正常驱动
2. 声卡ID 40
3. 有线网卡 正常
4. USB 3.0 2.0 正常
5. 睡眠正常
6. 唤醒正常
7. 关机正常
8. 无花屏现象
```

# 目前碰到问题
```
1. 开机读条会黑屏大约1~2秒，然后进入用户登录界面（好像只有核显都会有这毛病？）。
2. 核显DVI-I输出在10.15.5系统上，实测无法显示。
```

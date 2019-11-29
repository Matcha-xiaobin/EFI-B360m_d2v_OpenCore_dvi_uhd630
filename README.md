# EFI-B360m_d2v_OpenCore_dvi_uhd630
OC引导工具 EFI 配置文件

Open Core版本:  0.5.3 11/27 详情: [Open Core 最新自动编译版](https://github.com/williambj1/OpenCore-Factory)、[Open Core 官方版](https://github.com/acidanthera/OpenCorePkg/releases)

Clover引导文件请看这里：[Clover引导](https://github.com/Matchas-xiaobin/EFI-B360m_d2v_dvi_uhd630)

```
机器配置:
处理器: i5-8400
主板: 技嘉 B360m d2v
内存: 16G
显卡: UHD630(核显)
声卡: 内建Realtek® ALC887芯片
网卡: 内建Realtek® GbE 网络芯片(10/100/1000 Mbit)
无线网卡: 无
```

# 目前进度
```
1. 核显DVI输出，显存1536M
2. 声卡ID 11
3. 有线网卡 正常
4. USB 3.0 2.0 正常
   USB这个需要定制，可能在别的同型号电脑上不正常
5. 睡眠正常
6. 唤醒正常
7. 关机正常
8. 无花屏现象
```

# 目前碰到问题
```
暂无（暂未发现，如有发现问题，可以告知我一下，谢谢）
```

# 其他问题   
```
1. macOS版本:  10.15.1
2. 通过DVI或者VGA输出实测都可以
3. 不保证一定能用，不会搞，全是在网上找别的大佬的文件后折腾，在自己电脑上是可以正常运行了。
4. 安装镜像是用的 黑果小兵 的二合一镜像，搜索 黑果小兵 就可以找到，里面有很多教程。
5. 没有尝试麦克风是否可用，因为没有麦克风设备。
6. 如果你的USB3.0或者2.0用不了，请自行定制USB3.0，因为有可能会端口不一样。
7. 如果开机鼠标键盘都无法使用，请删除: 
        OC/kexts/USBPorts.kext;
        并且在配置文件里删掉这个kext。
        然后再次开机后去定制USB驱动。
```

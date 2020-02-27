# 解锁CFG Lock
```
[GIGABYTE B360m d2v 主板官网](https://www.gigabyte.cn/Motherboard/B360M-D2V-rev-10/sp#sp)

1.首先把这个EFI放在EFI分区下（U盘或者硬盘的都可以，注意备份原来的EFI文件夹）;
2.重启电脑选择从这个EFI所在的盘启动;
3.使用命令: setup_var_3 0x5C1 0x00 即可;

注意:
如有不明白, 请去百度。
主板型号不一样的话, 可能会无效, 并且可能引发某些不可预料的问题。

请自行百度了解各种风险之后在继续。
```

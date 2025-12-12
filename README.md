### 机场推荐 [ENET--IEPL内网专线接入](https://www.easyenable.com/#/register?code=CNC7La7m)
# OpenWrt — Marvell多设备固件云编译


### 固件默认配置
- 默认eth0(10G网口1)和eth2(2.5G网口1)桥接作为WAN接口
- 用户名：`root` 密码：`password` 管理IP：`192.168.11.1`
- 下载地址：https://github.com/DHDAXCW/OpenWrt_Marvell/releases 对应 Tag 标签内下载固件
- 电报交流群：https://t.me/armopenwrt

### 固件特色
1. 集成 iStore 应用商店，可根据自己需求自由安装所需插件
2. 集成应用过滤插件，支持游戏、视频、聊天、下载等 APP 过滤
3. 集成在线用户插件，可查看所有在线用户 IP 地址与实时速率等
4. 集成部分常用有线、无线、3G / 4G /5G 网卡驱动 可在issues提支持网卡，看本人能力了。。。
5. 支持在线更新，从2024.03.27之后就能通过后台升级
<img width="2040" height="1984" alt="e74733eb-1e51-4a86-a225-b2ae905528d8" src="https://github.com/user-attachments/assets/9e2045e4-63ae-4b3a-91f0-ed9f5b2e8321" />
<img width="2604" height="1574" alt="f0ae96afd82202a460766be472eb63b7" src="https://github.com/user-attachments/assets/7a004b12-7116-40ec-8a38-bd476d586fb7" />

### 如果在刷机过程中遇到插入nvme导致kernel无法加载，使用ttl在uboot模式下可执行以下命令解决此问题
```bash
qhora-322执行下面命令
setenv bootcmd 'ext4load mmc 0:1 0x6500000 Image; ext4load mmc 0:1 0x6000000 cn9132-qhora-322.dtb; setenv bootargs $console cpuidle.off=1; booti 0x6500000 - 0x6000000'; saveenv; reset

qhora-321执行下面命令
setenv bootcmd 'ext4load mmc 0:1 0x6500000 Image; ext4load mmc 0:1 0x6000000 cn9130-qhora-321.dtb; setenv bootargs $console cpuidle.off=1; booti 0x6500000 - 0x6000000'; saveenv; reset
```
### 特别提示 [![](https://img.shields.io/badge/-个人免责声明-FFFFFF.svg)](#特别提示-)

- **因精力有限不提供任何技术支持和教程等相关问题解答，不保证完全无 BUG！**

- **本人不对任何人因使用本固件所遭受的任何理论或实际的损失承担责任！**

- **本固件禁止用于任何商业用途，请务必严格遵守国家互联网使用相关法律规定！**

### 有bug请在 https://github.com/DHDAXCW/OpenWrt_Marvell/issues 提问题

### 鸣谢

特别感谢以下项目：

Openwrt 官方项目：

<https://github.com/openwrt/openwrt>

Lean 大的 Openwrt 项目：

<https://github.com/coolsnowwolf/lede>

immortalwrt 的 OpenWrt 项目：

<https://github.com/immortalwrt/immortalwrt>

P3TERX 大佬的 Actions-OpenWrt 项目：

<https://github.com/P3TERX/Actions-OpenWrt>

SuLingGG 大佬的 Actions 编译框架 项目：

https://github.com/SuLingGG/OpenWrt-Rpi

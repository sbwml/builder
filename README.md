<p align="center">
  <img width="400px" src="https://github.com/user-attachments/assets/6d37cd69-a232-4444-9f91-30e5942a8938" />
</p>

<h1 align="center">OpenWrt for FriendlyElec NanoPi R4S / R5S & X86_64 & Netgear R8500</h1>

<p align="center">
  <img width="300px" src="https://cdn.cooluc.com/r4s/r5s_.webp" />
</p>

<p align="center">
  <b>基于原生 <a href="https://github.com/openwrt/openwrt" target="_blank" >OpenWrt</a> 更改与优化的固件，提供高效、稳定的使用体验！</b>
</p>

-------

## 固件下载

**NanoPi R4S: https://r4s.cooluc.com**

**NanoPi R5S: https://r5s.cooluc.com**

**X86_64: https://x86.cooluc.com**

**Netgear R8500: https://r8500.cooluc.com**

**Snapshot-24.10: https://snapshot.cooluc.com**

## 版本信息

**[Releases](https://r5s.cooluc.com/releases)：正式版 - 基于 [OpenWrt](https://github.com/openwrt/openwrt/releases) 最新 Releases 源代码和软件包编译（推荐） - [Linux 6.12 LTS](https://kernel.org/)**

**[Snapshots](https://r5s.cooluc.com/snapshots)：开发版 - 基于 [OpenWrt](https://github.com/openwrt/openwrt/tree/openwrt-23.05) 最新 openwrt-23.05 分支源代码和软件包编译 - [Linux 6.12 LTS](https://kernel.org/)（每夜构建）**

**[Minimal](https://r5s.cooluc.com/minimal)：轻量版 - 基于 [OpenWrt](https://github.com/openwrt/openwrt/releases) 最新 Releases 源代码和软件包编译，无内置插件（不推荐） - [Linux 6.12 LTS](https://kernel.org/)**

------

## 默认信息

- **管理地址：[http://10.0.0.1](http://10.0.0.1) 或 [http://openwrt.lan](http://openwrt.lan)**
- **账户：root**
- **密码：无**

------

## 基本状况

| 基本                                              | 状态 | 基本                         | 状态 |
|:-------------------------------------------------:|:----:|:----------------------------:|:----:|
| kmod 内核模块安装                                 | ✅   | 全锥型 NAT（NFT、BCM 双方案）| ✅   |
| SS AES 硬件加速                                   | ✅   | 构建优化（O3、LTO）          | ✅   |
| GPU 硬件加速                                      | ✅   | 内核/模块 优化（LLVM LTO）   | ✅   |
| HDMI 终端输出                                     | ✅   | 在线 OTA 升级（squashfs）    | ✅   |
| RTC 时钟 (HYM8563)                                | ✅   | 固件重置（squashfs）         | ✅   |
| BBRv3 拥塞控制                                    | ✅   | LLVM-BPF 支持                | ✅   |
| KVM 虚拟化加速                                    | ✅   | Shortcut-FE（支持 UDP 入站）  | ✅   |
| NGINX & CURL HTTP3/QUIC 支持                      | ✅   | LRNG（v54）                  | ✅   |
| TCP Brutal 拥塞控制                               | ✅   |                             |      |

| 内置插件                 | 状态 | 内置插件         | 状态 |
|:------------------------:|:----:|:----------------:|:----:|
| PassWall                 | ✅   | Docker           | ✅   |
| ShadowSocksR Plus+       | ✅   | TTY 终端         | ✅   |
| HomeProxy                | ✅   | NetData 监控     | ✅   |
| FileBrowser              | ✅   | DiskMan 磁盘管理 | ✅   |
| qBittorrent              | ✅   | CPU 性能调节     | ✅   |
| MosDNS                   | ✅   | SQM 列队管理     | ✅   |
| 动态 DNS                 | ✅   | nlbw 宽带监控    | ✅   |
| Watchcat                 | ✅   | Socat            | ✅   |
| KMS 服务器               | ✅   | 应用过滤         | ✅   |
| FRP 客户端               | ✅   | 访问控制         | ✅   |
| 网络唤醒                 | ✅   | UPnP             | ✅   |
| 网络共享（Samba）        | ✅   | IP 限速          | ✅   |
| 锐捷认证                 | ✅   | WireGuard        | ✅   |
| Aria2                    | ✅   | L2TP             | ✅   |
| Alist 文件列表           | ✅   | ZeroTier         | ✅   |
| USB 打印服务器           | ✅   | GoWebDav         | ✅   |
| AirConnect               | ✅   | AirPlay 2        | ✅   |
| 自定义命令               | ✅   | 网速测试         | ✅   |

✅ 可用

❌ 不可用

⏳ 计划中

特别说明：

* *AirPlay 2：一款简单易用的 AirPlay 音频播放器，需要外接 USB 声卡使用。*
* *Shortcut-FE：当使用 “Shortcut-FE 流量分载” 时，请先关闭 “软件流量分载”。*

<details>
<summary><b>LuCI 菜单概览</b></summary>
<details>
<summary><b>├── 状态</b></summary>
　├── 概览<br/>
　├── 路由<br/>
　├── 防火墙<br/>
　├── 路由表<br/>
　├── 系统日志<br/>
　├── 系统进程<br/>
　├── 实时信息<br/>
　├── 实时监控<br/>
　├── 在线用户<br/>
　├── WireGuard<br/>
　└── 释放内存
</details>
<details>
<summary><b>├── 系统</b></summary>
　├── 系统<br/>
　├── 管理权<br/>
　├── 软件包<br/>
　├── 启动项<br/>
　├── 计划任务<br/>
　├── 挂载点<br/>
　├── 终端<br/>
　├── 磁盘管理<br/>
　├── LED 配置<br/>
　├── 在线升级<br/>
　├── 备份/升级<br/>
　├── 自定义命令<br/>
　├── 定时重启<br/>
　├── Argon 主题设置<br/>
　├── CPU 性能调节<br/>
　└── 重启
</details>
<details>
<summary><b>├── 服务</b></summary>
　├── PassWall<br/>
　├── HomeProxy<br/>
　├── qBittorrent<br/>
　├── MosDNS<br/>
　├── 动态 DNS(DDNS)<br/>
　├── Watchcat<br/>
　├── 文件浏览器<br/>
　├── KMS 服务器<br/>
　├── 隔空播放<br/>
　├── AirPlay 2 播放器<br/>
　├── Aria2<br/>
　├── FRP 客户端<br/>
　├── 锐捷认证<br/>
　├── 网络共享<br/>
　├── 网络唤醒<br/>
　└── ZeroTier
</details>
<details>
<summary><b>├── Docker</b></summary>
　├── 概览<br/>
　├── 容器<br/>
　├── 镜像<br/>
　├── 网络<br/>
　├── 卷标<br/>
　├── 事件<br/>
　└── 配置
</details>
<details>
<summary><b>├── 网络存储</b></summary>
　├── Alist 文件列表<br/>
　├── USB 打印服务器<br/>
　└── GoWebDav
</details>
<details>
<summary><b>├── 网络</b></summary>
　├── 接口<br/>
　├── 路由<br/>
　├── DHCP/DNS<br/>
　├── 网络诊断<br/>
　├── SQM 队列管理<br/>
　├── 防火墙<br/>
　├── UPnP<br/>
　├── 带宽监控<br/>
　├── 网速测试<br/>
　├── 应用过滤<br/>
　├── Socat<br/>
　├── 访问控制<br/>
　└── IP 限速
</details>
　└── <b>退出</b>
</details>

------

## 固件格式

**固件分为两个文件系统，[SquashFS](https://zh.wikipedia.org/wiki/SquashFS) 和 [Ext4](https://zh.wikipedia.org/wiki/Ext4)。**

**SquashFS（推荐）：固件文件名带有 “squashfs”，SquashFS 为只读文件系统，支持系统重置，更能避免 SD 卡文件系统触发写保护，支持在线 OTA 升级，适合绝大部分用户使用。**

**Ext4：固件文件名带有 “ext4”，Ext4 文件系统具备整个分区可读写性质，更适合熟悉 Linux 系统的用户使用，但意外断电有几率造成分区写入保护。**


------

## NanoPi R4S/R5S 固件烧写（SD）

**推荐工具：**<a href="https://www.balena.io/etcher/" target="_blank" ><img style="height:25px;" src="https://cdn.cooluc.com/r4s/balena.svg" /></a>

**SD卡容量：2GB 或更多**

*固件文件无需解压，直接使用工具写入 microSD 卡*

------

## 固件烧写（NanoPi R5S eMMC）

### 准备工具

- **电脑（Windows），其它操作系统自行搜索相关工具**
- **数据线：USB-A to USB-A 或 Type-C to USB-A**
- **瑞芯微开发工具：**<a href="https://media.cooluc.com/%E8%BD%AF%E4%BB%B6/RKDevTool/RKDevTool_Release_v2.84.zip" target="_blank" >RKDevTool_Release_v2.84.zip</a>

- **Mask 设备驱动：**<a href="https://media.cooluc.com/%E8%BD%AF%E4%BB%B6/RKDevTool/DriverAssitant_v5.1.1.zip" target="_blank" >DriverAssitant_v5.1.1.zip</a>

### 准备固件

- **下载固件文件，并解压出 .img**

### 操作过程

- **安装 Mask 设备驱动**

- **Mask 模式连接电脑（R5S 断电状态下，取下 SD 卡，使用数据线连接电脑。长按 “Mask” 按钮，接通 R5S 电源直至电脑发现新设备后释放 “Mask” 按钮）**

  <img style="height:100px;" src="https://cdn.cooluc.com/r4s/r5s_mask.webp" />



- **打开 瑞芯微开发工具：正常状态：（发现一个Maskrom设备）  缺少驱动：（没有发现设备）**

  **安装步骤：**
  
  **① 点击 “system” 路径选择按钮（选择 zip 解压出来的 IMG 文件）**
  
  <img src="https://cdn.cooluc.com/r4s/select_firmware.png" />
  
  
  
  **② 点击 “执行”（固件写入完成后会自动重启进入 OpenWrt 系统）**
  
  
  
- ***注意：通过电脑烧写固件请使用本站下载的 [瑞芯微开发工具](https://media.cooluc.com/%E8%BD%AF%E4%BB%B6/RKDevTool/RKDevTool_Release_v2.84.zip)。***

------

## 固件烧写（SD to eMMC）

```shell
# 通过 SD 卡启动后，上传固件文件到路由器任意目录（需要空间大于2G），比如 /tmp 目录，并执行以下命令将固件写入到 eMMC 存储
# 可以使用 SFTP 工具上传固件到 /tmp 目录，或通过终端 wget 在线下载固件到 /tmp 目录

# 进入 tmp 目录
cd /tmp

# 解压 img 固件（请根据实际文件名称）
gzip -d openwrt-23.05.3-rockchip-armv8-friendlyarm_nanopi-r5s-squashfs-sysupgrade.img.gz

# 写入 img 固件到 eMMC 存储（of=/dev/mmcblk1 改成你的 eMMC 存储实际路径，fdisk -l 命令可查看具体路径）
dd if=openwrt-23.05.3-rockchip-armv8-friendlyarm_nanopi-r5s-squashfs-sysupgrade.img of=/dev/mmcblk1 bs=1M oflag=dsync

```

**固件写入完成后，取下 SD 卡，手动断电重启即可完成。**

------

## RTC 硬件时钟（HYM8563）

**本固件支持 RTC 硬件时钟读取/同步，当设备断电时，重新通电启动系统时间不会错乱** *（注意：设备需要安装 RTC 电池后使用）*

**首次安装 RTC 电池写入时间命令**

```shell
hwclock -w -f /dev/rtc1
```

**测试时间读取（返回当前时间表示正常）**

```shell
hwclock -f /dev/rtc1
```

------

## 开源地址

**构建脚本：** [https://init2.cooluc.com](https://init2.cooluc.com)

**构建脚本（存档）：** [https://github.com/sbwml/r4s_build_script](https://github.com/sbwml/r4s_build_script)

**构建来源：** [https://github.com/sbwml/builder](https://github.com/sbwml/builder)

# AutoBuild-OpenWrt
[![LICENSE](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat&logo=github&label=LICENSE)](https://github.com/esirplayground/AutoBuild-OpenWrt/blob/master/LICENSE)
![GitHub Stars](https://img.shields.io/github/stars/esirplayground/AutoBuild-OpenWrt.svg?style=flat&logo=appveyor&label=Stars&logo=github)
![GitHub Forks](https://img.shields.io/github/forks/esirplayground/AutoBuild-OpenWrt.svg?style=flat&logo=appveyor&label=Forks&logo=github)
![GitHub last commit](https://img.shields.io/github/last-commit/esirplayground/AutoBuild-OpenWrt?label=Latest%20Commit&logo=github)

Build OpenWrt firware [Lean's OpenWrt](https://github.com/coolsnowwolf/lede) using GitHub Actions  
Hereby thank P3TERX for his amazing job: https://github.com/P3TERX/Actions-OpenWrt/  

Hereby thank KFERMercer for his amazing job: https://github.com/KFERMercer/OpenWrt-CI  
You could edit and enable "Sync Code" YAML file to let your forked repo keep updated.

## Usage

🔥🔥[Video Tutorial (in Mandrin) | 视频教程(国语)](https://youtu.be/9YO7nxNry-4)📺🎉

**1. Prerequisite**
  - Sign up for [GitHub Actions](https://github.com/features/actions/signup)
  - Fork [this GitHub repository](https://github.com/esirplayground/AutoBuild-OpenWrt)
    
**2. Compile Firmware**
  - Click `[.github/workflows]` folder on the top of repo and you could see few workflow files, Each for one particular architecture(device).
  - ***`UPDATED`*** Click "Action" on the menu, click your favoriate device on the left side, then go to the right side "Run workflow" button, click and on the dropdown menu, click the green button "Run workflow", that's it!!
  - The build starts automatically. Progress can be viewed on the Actions page.
  - When the build is complete, click the `Artifacts` button in the upper right corner of the Actions page to download the binaries.
  - Default Web Admin IP: `192.168.5.1`, username `root`, no login password

**3. Sync Code**
  - Uncomment 'push-branches-master' 3 lines under **`On`** section and commit changes to let the script sync the code once for you.
  - Uncomment 'schedule-cron' 2 lines under **`On`** section and commit changes to let the script sync the code everyday on 3 am[UTC +8]

## Plugins

**1. Extra packages**
  - ipv6helper

**2. Applications**
  - luci-app-accesscontrol 访问控制
  - luci-app-argon-config Argon主题配置插件
  - luci-app-arpbind IP/MAC绑定
  - luci-app-autoreboot 支持计划重启
  - luci-app-diskman 磁盘管理工具
    - lsblk 列出所有可用块设备的信息
  - luci-app-docker Docker容器
  - luci-app-dockerman Dockerman容器
  - luci-app-filetransfer 文件传输（可web安装ipk包）
  - luci-app-firewall 添加防火墙
  - uci-app-nlbwmon 网络带宽监视器
  - luci-app-ntpc NTP时间同步服务器
  - luci-app-rclone 命令行云端同步工具
    - rclone-webui Rclone界面
    - rclone-ng (another webui) Rclone另一个界面
  - luci-app-socat 多功能的网络工具(端口转发)
  - luci-app-smartdns SmartDNS本地服务器
  - luci-app-turboacc Turbo ACC 网络加速(支持 Fast Path 或者 硬件 NAT)
    - Include Shortcut-FE Shortcut-FE 流量分载
    - Include BBR CCA BBR拥塞控制算法提升TCP网络性能
    - Include Pdnsd DNS防污染
  - luci-app-upnp 通用即插即用UPnP（端口自动转发）

**3. Theme**
  - luci-theme-argon-mod

**3. Network**
  - ip6tables-extra
  - ip6tables-mod-nat
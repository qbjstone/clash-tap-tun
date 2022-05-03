# Clash TAP TUN 区别和使用方法

Clash 软件下载地址：https://github.com/Fndroid/clash_for_windows_pkg/releases<br>
视频教程：▶ https://youtu.be/V1oSmz1k29Y

### 启动 TAP 模式

    dns:
      enable: true
      enhanced-mode: redir-host # 或 fake-ip
      listen: 0.0.0.0:53
      nameserver:
        - 223.5.5.5
        
# 常见问题
### Clash Tap Device 虚拟网卡 是什么？
因为有些软件不走系统代理，就算我们开启了翻墙，也不能让这些软件走翻墙。<br>

例如：有些游戏软件，就算开启了翻墙也不能实现加速。<br>
这个时候就需要用另外的模式翻墙，让所有的流量走虚拟网卡，实现真正的全局翻墙模式。<br>
我们可以用 Clash Tap 虚拟网卡模式，实现所有软件代理。<br><br>

### Clash TUN Mode 是什么?
让电脑所有的流量都走虚拟网卡，实现全局代理，和TAP模式类似。<br><br>

### Clash TAP TUN 区别？
Clash TUN 和 TAP 类似，都是让所有流量走虚拟网卡，实现所有软件翻墙，但TUN 模式性能比 TAP 模式好，所以更推荐使用 TUN 模式。<br><br>

### 什么情况下需要开启 TAP/TUN ？
我们平时使用浏览器翻墙，比如访问google网站，或者使用一些遵循系统代理的软件时，不需要开启 TAP/TUN 模式。<br>
在使用一些游戏软件需要加速，或者一些不遵循系统代理的软件时，需要开启 TAP/TUN 模式。 <br><br>

### 使用 Clash TAP/TUN 支持规则吗？
支持规则，可以实现国内网站走直连，国外网站走代理等。<br><br>

### Clash Service Mode是什么？
需要在 Service Mode 安装，才能使用 TUN 模式。<br><br>

### Clash TAP 网络电缆被拔出
出现这种提示表示没有启动 TAP模式，只需要启动 TAP 模式即可。<br><br>

### Service Mode 无法安装
视频教程：▶ https://youtu.be/_zO-8R_tgaE<br>
.NET framework  <a href="https://dotnet.microsoft.com/zh-cn/download/dotnet-framework/net48" target="_blank">点击下载>></a><br>

然后尝试手动安装：<br>
1、关闭360等杀毒软件<br>
2、点击 General 中的 Home Directory 打开文件夹，进入 service 子目录中<br>
3、打开 CMD，执行以下命令：<br>

    service.exe install
    service.exe start


### Killer 系列网卡无法开启 TAP/TUN 模式
对于 Killer 系列网卡，需要在 Killer Control Center 中，关闭「Killer Prioritization Engine」才可以使用 Clash 的 TUN 或者 TAP。<br><br>


### 在 Windows 系统中，TUN 模式下无法使用热点分享功能
1、开启热点分享功能，此时系统网络设置中会生成一个网卡<br>
2、开启 TUN 模式<br>
3、进入系统网络设置，在 Clash 网卡右键选择属性，选择共享标签页<br>
4、勾选“允许其他网络用户通过此计算机的 Internet 连接来连接”<br>
5、在“家庭网络连接”选择框中选择第 1 步生成的网卡<br><br>


### 软件启动时，TUN 创建网卡失败，提示 Start Tun interface error: error creating interface: Cannot create a file when that file already exists.
1、进入 Home Directory<br>
2、编辑 config.yaml，添加如下配置（在最后面粘贴）：<br>

    tun:
      enable: true
      stack: gvisor
      auto-route: false
      auto-detect-interface: false
3、重启 Clash
  



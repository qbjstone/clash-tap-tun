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

### Clash TAP 网络适配器 无法安装？
如果无法安装 TAP ，可以尝试这样安装：
- 先开启翻墙再安装。
- 重启电脑再安装。
- 将电脑网卡驱动卸载重新安装。




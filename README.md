# hebei-iptv
河北电信IPTV组播源

2024/02/24更新，亲测可用

以下为代理链接

- `https://mirror.ghproxy.com/raw.githubusercontent.com/akumajac/hebei-iptv/main/单播.txt`
- `https://mirror.ghproxy.com/raw.githubusercontent.com/akumajac/hebei-iptv/main/组播.txt`
- 这个有点问题 `https://mirror.ghproxy.com/raw.githubusercontent.com/akumajac/hebei-iptv/main/tvbox-test.txt`

## 参考教程
本教程参考自B站up主[maxdarksol](https://www.bilibili.com/read/cv18776837)

1、光猫取消端口绑定，划分vlan，我将上网口划分1，iptv划分为2
   河北于23年末左右强制更换光猫管理员密码，需要抓包
2、openwrt路由器新建接口，自定义接口填上：wan口的标识符 加上.iptv划分的vlan名称。如我的wan口是eth1，那么我就填上eth1.2
![Uploading 屏幕截图 2024-03-06 213259.png…]()  ![Uploading 屏幕截图 2024-03-06 213406.png…]()







## 公益源推荐
> 茶客公益源[项目地址](https://github.com/vamoschuck/TV)**/**[下载链接](https://raw.githubusercontent.com/vamoschuck/TV/main/M3U)
> 
> 
> 

### 自用备忘

- 192.168.28.0/24     
192.168.28.9 为内网回看地址
  
例rtsp://192.168.28.9/PLTV/88888914/224/3221225729/10000100000000060000000000000636_0.smil?playseek=20200306204239-2020030622330

- **option60 Vendor Class：** `HEITV`
- **option12 host name：** `机顶盒的STBID`

- **河北电信机顶盒操作码** `1301`

- **itv密码** `118114`

- **组播查找正则表达式：**`ChannelName="(.*?)".*?(igmp://.*?)\|rtsp`

- **单播查找正则表达式：**`ChannelName="(.*?)".*?(rtsp://.*?smil)`

- **替换表达式：**`$1,$2`

- **在线表达式**
  > [正则表达式在线工具](https://tool.oschina.net/regex)
- **直播源列表转换工具**
  > [M3U转换](https://guihet.com/tvlistconvert.html)
- **EPG频道列表**
  > [epg转换51zmt](http://epg.51zmt.top:8000/)
  > 
  > [112114](https://epg.112114.eu.org/)



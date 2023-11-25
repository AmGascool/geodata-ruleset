# 一、 说明
- 注：可[点此](https://github.com/DustinWin/clash-geosite/tree/domains)查看包含的域名列表

## 1. geosite-all.dat 和 geosite-all.db（适用于使用了 [sing-box 平台](https://github.com/SagerNet/sing-box)的客户端，下同）
① 根据 [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat) 进行深度定制，**有且仅有如下分类**：
```
  - GEOSITE,ads,⛔️ 广告域名
  - GEOSITE,private,🏠 私有网络
  - GEOSITE,microsoft-cn,Ⓜ️ Microsoft 中国
  - GEOSITE,apple-cn,🍎 Apple 中国
  - GEOSITE,google-cn,🗽 Google 中国
  - GEOSITE,games-cn,🎮 国区游戏
  - GEOSITE,netflix,🎥 Netflix
  - GEOSITE,disney,📽️ Disney+
  - GEOSITE,max,🎞️ Max
  - GEOSITE,primevideo,🎬 Prime Video
  - GEOSITE,appletv,🍎 Apple TV+
  - GEOSITE,youtube,📹 YouTube
  - GEOSITE,tiktok,🎵 TikTok
  - GEOSITE,bilibili,📺 哔哩哔哩
  - GEOSITE,openai,🤖 人工智能
  - GEOSITE,networktest,📈 网络测试
  - GEOSITE,proxy,🪜 代理域名
  - GEOSITE,cn,⚡ 直连域名
```
② 每天早上 3 点（北京时间）自动构建  
③ `geosite:ads` 源采用 [privacy-protection-tools/anti-AD/anti-ad-domains.txt](https://github.com/privacy-protection-tools/anti-AD)  
④ `geosite:private` 源采用 [v2fly/domain-list-community/private](https://github.com/v2fly/domain-list-community/blob/master/data/private) 和 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan) 组合，并添加主流 Clash dashboard 在线面板域名（`clash.razord.top`、`clash.metacubex.one`、`yacd.haishan.me`、`yacd.metacubex.one` 和 `d.metacubex.one`）  
⑤ `geosite:microsoft-cn` 源采用 [v2fly/domain-list-community/microsoft@cn](https://github.com/v2fly/domain-list-community/blob/master/data/microsoft)  
⑥ `geosite:apple-cn` 源采用 [felixonmars/dnsmasq-china-list/apple.china.conf](https://github.com/felixonmars/dnsmasq-china-list)  
⑦ `geosite:google-cn` 源采用 [felixonmars/dnsmasq-china-list/google.china.conf](https://github.com/felixonmars/dnsmasq-china-list)  
⑧ `geosite:games-cn` 源采用 [v2fly/domain-list-community/category-games@cn](https://github.com/v2fly/domain-list-community/blob/master/data/category-games)、[blackmatrix7/ios_rule_script/SteamCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/SteamCN) 和 [blackmatrix7/ios_rule_script/GameDownloadCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Game/GameDownloadCN) 组合  
⑨ `geosite:netflix` 源采用 [blackmatrix7/ios_rule_script/Netflix](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)  
⑩ `geosite:disney` 源采用 [blackmatrix7/ios_rule_script/Disney](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Disney)  
⑪ `geosite:max` 源采用 [blackmatrix7/ios_rule_script/HBO](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/HBO)  
⑫ `geosite:primevideo` 源采用 [blackmatrix7/ios_rule_script/PrimeVideo](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/PrimeVideo)  
⑬ `geosite:appletv` 源采用 [blackmatrix7/ios_rule_script/AppleTV](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/AppleTV)  
⑭ `geosite:youtube` 源采用 [blackmatrix7/ios_rule_script/YouTube](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/YouTube)  
⑮ `geosite:tiktok` 源采用 [blackmatrix7/ios_rule_script/TikTok](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/TikTok)  
⑯ `geosite:bilibili` 源采用 [blackmatrix7/ios_rule_script/BiliBili](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/BiliBili)  
⑰ `geosite:openai` 源采用 [blackmatrix7/ios_rule_script/OpenAI](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/OpenAI)  
⑱ `geosite:networktest` 源采用 [blackmatrix7/ios_rule_script/Speedtest](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Speedtest) 和 IPv6 测试网站（采用 `keyword` 关键字）组合    
⑲ `geosite:proxy` 源采用 [cokebar/gfwlist2dnsmasq](https://github.com/cokebar/gfwlist2dnsmasq) 生成的 [gfwlist](https://github.com/gfwlist/gfwlist) 和 [blackmatrix7/ios_rule_script/Proxy](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Proxy) 组合  
⑳ `geosite:cn` 源采用 [blackmatrix7/ios_rule_script/ChinaMax](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)
## 2. geosite-all-lite.dat 和 geosite-all-lite.db
在 geosite-all.dat 和 geosite-all.db 的基础上去除了广告域名 `geosite:ads`，**有且仅有如下分类**：
```
  - GEOSITE,private,🏠 私有网络
  - GEOSITE,microsoft-cn,Ⓜ️ Microsoft 中国
  - GEOSITE,apple-cn,🍎 Apple 中国
  - GEOSITE,google-cn,🗽 Google 中国
  - GEOSITE,games-cn,🎮 国区游戏
  - GEOSITE,netflix,🎥 Netflix
  - GEOSITE,disney,📽️ Disney+
  - GEOSITE,max,🎞️ Max
  - GEOSITE,primevideo,🎬 Prime Video
  - GEOSITE,appletv,🍎 Apple TV+
  - GEOSITE,youtube,📹 YouTube
  - GEOSITE,tiktok,🎵 TikTok
  - GEOSITE,bilibili,📺 哔哩哔哩
  - GEOSITE,openai,🤖 人工智能
  - GEOSITE,networktest,📈 网络测试
  - GEOSITE,proxy,🪜 代理域名
  - GEOSITE,cn,⚡ 直连域名
```
## 3. geosite.dat 和 geosite.db
在 geosite-all.dat 和 geosite-all.db 的基础上去除了流媒体和人工智能 `geosite:openai`，**有且仅有如下分类**：
```
  - GEOSITE,ads,⛔️ 广告域名
  - GEOSITE,private,🏠 私有网络
  - GEOSITE,microsoft-cn,Ⓜ️ Microsoft 中国
  - GEOSITE,apple-cn,🍎 Apple 中国
  - GEOSITE,google-cn,🗽 Google 中国
  - GEOSITE,games-cn,🎮 国区游戏
  - GEOSITE,networktest,📈 网络测试
  - GEOSITE,proxy,🪜 代理域名
  - GEOSITE,cn,⚡ 直连域名
```
## 4. geosite-lite.dat 和 geosite-lite.db
在 geosite.dat 和 geosite.db 的基础上去除了广告域名 `geosite:ads`，**有且仅有如下分类**：
```
  - GEOSITE,private,🏠 私有网络
  - GEOSITE,microsoft-cn,Ⓜ️ Microsoft 中国
  - GEOSITE,apple-cn,🍎 Apple 中国
  - GEOSITE,google-cn,🗽 Google 中国
  - GEOSITE,games-cn,🎮 国区游戏
  - GEOSITE,networktest,📈 网络测试
  - GEOSITE,proxy,🪜 代理域名
  - GEOSITE,cn,⚡ 直连域名
```
## 5. geoip-all.dat、Country-all.mmdb、geoip-all.metadb 和 geoip-all.db
① 源采用 [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip)，包含如下分类（可[点此](https://github.com/Loyalsoldier/geoip/tree/release/text)查看其它国家或地区 IP 规则集）：
```
  - GEOIP,cloudflare,☁️ Cloudflare
  - GEOIP,cloudfront,🌐 CloudFront
  - GEOIP,facebook,👓 Facebook
  - GEOIP,fastly,🌎 Fastly
  - GEOIP,google,🗽 Google
  - GEOIP,netflix,🎥 Netflix
  - GEOIP,telegram,✈️ Telegram
  - GEOIP,twitter,💬 Twitter
  - GEOIP,cn,🇨🇳 国内 IP
```
② .metadb 规则集文件适用于使用了 [Clash.Meta 内核](https://github.com/MetaCubeX/Clash.Meta)的客户端（下同）
## 6. geoip.dat、Country.mmdb、geoip.metadb 和 geoip.db
① 根据 Loyalsoldier/geoip 进行深度定制，**有且仅有如下分类**：
```
  - GEOIP,netflix,🎥 Netflix
  - GEOIP,telegram,✈️ Telegram
  - GEOIP,private,🏠 私有网络
  - GEOIP,cn,🇨🇳 国内 IP
```
② 每天早上 3 点（北京时间）自动构建  
③ `geoip:netflix` 源采用 [blackmatrix7/ios_rule_script/Netflix/Netflix_IP.txt](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)  
④ `geoip:telegram` 源采用 [Telegram IP](https://core.telegram.org/resources/cidr.txt)   
⑤ `geoip:private` 源采用 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（IP 部分）  
⑥ `geoip:cn` 源采用 [GeoLite2/cn.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[17mon/china_ip_list](https://github.com/17mon/china_ip_list)、[gaoyifan/china-operator-ip](https://github.com/gaoyifan/china-operator-ip) 和 [blackmatrix7/ios_rule_script/ChinaIPs/ChinaIPs_IP.txt](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaIPs) 组合
## 7. geoip-lite.dat、Country-lite.mmdb、geoip-lite.metadb 和 geoip-lite.db
分别在 geoip.dat、Country.mmdb、geoip.metadb 和 geoip.db 的基础上去除了流媒体，**有且仅有如下分类**：
```
  - GEOIP,telegram,✈️ Telegram
  - GEOIP,private,🏠 私有网络
  - GEOIP,cn,🇨🇳 国内 IP
```
## 8. user.yaml
① 每天早上 3 点（北京时间）自动构建生成  
② 添加[常用 fake-ip 地址过滤列表](https://github.com/juewuy/ShellClash/blob/master/public/fake_ip_filter.list)到 fake-ip-user.yaml 内的 `fake-ip-filter` 中，提高兼容性  
③ 添加 [TrackersList](https://trackerslist.com)（udp 域名）到 fake-ip-user.yaml 内的 `fake-ip-filter` 中，防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition/releases)无法连接 TrackersList UDP 协议  
<img src="https://user-images.githubusercontent.com/45238096/224113233-4d76dec2-495c-4790-a00e-538fc1469639.png" width="60%"/>  
④ 添加如下域名，以配合 AdGuardHome 作为下游时解决下载“DNS 黑名单”失败的问题：
```
    - 'adguardteam.github.io'
    - 'anti-ad.net'
```
⑤ 若想自己生成配置文件 user.yaml，可以 [Fork 本项目](https://github.com/DustinWin/clash-geosite/fork)后编辑 *.github/workflows/run.yml* 文件内的 `name: Generate xxx-user.yaml` 部分  
⑥ 若 DNS 模式选用的是 `redir-host`，需要进行 DNS 分流（可以参考《[ShellClash 使用 Clash.Meta 内核进行 DNS 分流教程-geox 方案](https://github.com/DustinWin/clash-tutorials/blob/main/%E6%95%99%E7%A8%8B%E5%90%88%E9%9B%86/%E8%BF%9B%E9%98%B6%E7%AF%87/ShellClash%20%E4%BD%BF%E7%94%A8%20Clash.Meta%20%E5%86%85%E6%A0%B8%E8%BF%9B%E8%A1%8C%20DNS%20%E5%88%86%E6%B5%81%E6%95%99%E7%A8%8B-geox%20%E6%96%B9%E6%A1%88.md)》），可以进入 *.github/workflows/run.yml* 文件，编辑 `Generate redir-host-user.yaml` 部分，将 `nameserver` 中的 `🪜 代理域名`改成可以访问外网的策略组名称，或者直接将 `'https://dns.google/dns-query#🪜 代理域名'` 修改为 `'tls://dns.google'`
# 二、 下载（以 geosite.dat、geosite.db、geoip.dat、Country.mmdb、geoip.metadb 和 geoip.db 为例）
## 1. geosite.dat
① GitHub 源：https://github.com/DustinWin/clash-geosite/releases/download/latest/geosite.dat  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite.dat
## 2. geosite.db
① GitHub 源：https://github.com/DustinWin/clash-geosite/releases/download/latest/geosite.db  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite.db
## 3. geoip.dat
① GitHub 源：https://github.com/DustinWin/clash-geosite/releases/download/latest/geoip.dat  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geoip.dat
## 4. Country.mmdb
① GitHub 源：https://github.com/DustinWin/clash-geosite/releases/download/latest/Country.mmdb  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/Country.mmdb
## 5. geoip.metadb
① GitHub 源：https://github.com/DustinWin/clash-geosite/releases/download/latest/geoip.metadb  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geoip.metadb
## 6. geoip.db
① GitHub 源：https://github.com/DustinWin/clash-geosite/releases/download/latest/geoip.db  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geoip.db
# 三、 导入（以 [ShellClash](https://github.com/juewuy/ShellClash) 导入 geosite.dat、geoip.dat 和 Country.mmdb 为例）
## 1. DNS 模式为 `fake-ip`  
连接 SSH 后执行如下命令：
```
curl -o $clashdir/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite.dat
curl -o $clashdir/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geoip.dat
curl -o $clashdir/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/Country.mmdb
curl -o $clashdir/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/fake-ip-user.yaml
$clashdir/start.sh restart
```
## 2. DNS 模式为 `redir-host`  
连接 SSH 后执行如下命令：
```
curl -o $clashdir/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite.dat
curl -o $clashdir/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geoip.dat
curl -o $clashdir/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/Country.mmdb
curl -o $clashdir/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/redir-host-user.yaml
$clashdir/start.sh restart
```

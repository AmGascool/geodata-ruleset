# 文件结构已经修改完成，描述文件待修改

# 一、 数据源说明
## 1. 规则集文件类型
① [Clash GeoX 规则集文件](https://github.com/DustinWin/ruleset_geox/tree/clash/geox)，包括：geosite.dat、Country.mmdb、geoip.dat 和 geoip.metadb 等  
② [Clash rule-set 规则集](https://github.com/DustinWin/ruleset_geox/tree/clash/ruleset)，格式为 `.yaml`  
③ [sing-box GeoX 规则集文件](https://github.com/DustinWin/ruleset_geox/tree/sing-box/geox)，包括：geosite.db 和 geoip.db 等  
④ [sing-box rule_set 规则集](https://github.com/DustinWin/ruleset_geox/tree/sing-box/ruleset)，格式有 `.json` 和 `.srs`
## 2. 数据源
- 注：请仔细核对规则名称与规则集文件的对应关系，以下方的[文件说明](https://github.com/DustinWin/ruleset_geox/blob/master/README.md)为准

① 每天凌晨 2 点半-3 点（北京时间）自动构建  
② `ads` 源采用 [privacy-protection-tools/anti-AD](https://github.com/privacy-protection-tools/anti-AD)  
③ `private` 源采用 [v2fly/domain-list-community/private](https://github.com/v2fly/domain-list-community/blob/master/data/private) 和 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan) 组合，并添加主流 [Clash dashboard 在线面板](https://github.com/DustinWin/clash_singbox-tools/tree/main/Clash-dashboard)域名（`clash.razord.top`、`clash.metacubex.one`、`yacd.haishan.me`、`yacd.metacubex.one` 和 `d.metacubex.one`）  
④ `microsoft-cn` 源采用 [v2fly/domain-list-community/microsoft@cn](https://github.com/v2fly/domain-list-community/blob/master/data/microsoft)  
⑤ `apple-cn` 源采用 [felixonmars/dnsmasq-china-list/apple.china.conf](https://github.com/felixonmars/dnsmasq-china-list)  
⑥ `google-cn` 源采用 [felixonmars/dnsmasq-china-list/google.china.conf](https://github.com/felixonmars/dnsmasq-china-list)  
⑦ `games-cn` 源采用 [v2fly/domain-list-community/category-games@cn](https://github.com/v2fly/domain-list-community/blob/master/data/category-games)、[blackmatrix7/ios_rule_script/SteamCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/SteamCN) 和 [blackmatrix7/ios_rule_script/GameDownloadCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Game/GameDownloadCN) 组合  
⑧ `netflix` 源采用 [blackmatrix7/ios_rule_script/Netflix](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)  
⑨ `disney` 源采用 [blackmatrix7/ios_rule_script/Disney](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Disney)  
⑩ `max` 源采用 [blackmatrix7/ios_rule_script/HBO](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/HBO)  
⑪ `primevideo` 源采用 [blackmatrix7/ios_rule_script/PrimeVideo](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/PrimeVideo)  
⑫ `appletv` 源采用 [blackmatrix7/ios_rule_script/AppleTV](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/AppleTV)  
⑬ `youtube` 源采用 [blackmatrix7/ios_rule_script/YouTube](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/YouTube)  
⑭ `tiktok` 源采用 [blackmatrix7/ios_rule_script/TikTok](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/TikTok)  
⑮ `bilibili` 源采用 [blackmatrix7/ios_rule_script/BiliBili](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/BiliBili)  
⑯ `ai` 源采用 [blackmatrix7/ios_rule_script/OpenAI](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/OpenAI)、[blackmatrix7/ios_rule_script/Bing](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Bing) 和 [blackmatrix7/ios_rule_script/BardAI](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/BardAI) 组合  
⑰ `networktest` 源采用 [blackmatrix7/ios_rule_script/Speedtest](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Speedtest) 和 IPv6 测试网站（采用 `keyword` 关键字，包括：`ipv6-test`、`test-ipv6`、`ipv6test` 和 `testipv6`）组合    
⑱ `proxy` 源采用 [cokebar/gfwlist2dnsmasq](https://github.com/cokebar/gfwlist2dnsmasq) 生成的 [gfwlist](https://github.com/gfwlist/gfwlist) 和 [Loyalsoldier/domain-list-custom/geolocation-!cn.txt](https://github.com/Loyalsoldier/domain-list-custom) 组合  
⑲ `cn` 源采用 [blackmatrix7/ios_rule_script/ChinaMax](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)，添加 `static.adtidy.org`，防止 [AdGuardHome](https://github.com/AdguardTeam/AdGuardHome) 作为下游时检查更新失败（在上游中必须使用国内 DNS 对其进行解析）  
⑳ `telegramip` 源采用 [Telegram IP 段](https://core.telegram.org/resources/cidr.txt)  
㉑ `privateip` 源采用 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（IP 部分）  
㉒ `cnip` 取自 [DustinWin/geoip](https://github.com/DustinWin/geoip)，源采用 [GeoLite2/cn.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[17mon/china_ip_list](https://github.com/17mon/china_ip_list)、[gaoyifan/china-operator-ip](https://github.com/gaoyifan/china-operator-ip) 和 [blackmatrix7/ios_rule_script/ChinaIPs/ChinaIPs_IP.txt](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaIPs) 组合  
注：
- 1. 可[点此](https://github.com/DustinWin/ruleset_geox/tree/master/Domains)查看包含的所有域名列表（ v2fly/domain-list-community/data 格式）
- 2. 可[点此](https://github.com/DustinWin/geoip/tree/master/IPs)查看包含的所有 IP 段列表

## 3. 文件说明
① geosite-all.dat 或 geosite-all.db  
包含的数据源最多，**有且仅有如下分类**：
```
  - GEOSITE,ads,🛑 广告拦截
  - GEOSITE,private,🔒 私有网络
  - GEOSITE,microsoft-cn,Ⓜ️ 微软服务
  - GEOSITE,apple-cn,🍎 苹果服务
  - GEOSITE,google-cn,📢 谷歌服务
  - GEOSITE,games-cn,🎮 游戏平台
  - GEOSITE,netflix,🎥 奈飞视频
  - GEOSITE,disney,📽️ 迪士尼+
  - GEOSITE,max,🎞️ Max
  - GEOSITE,primevideo,🎬 Prime Video
  - GEOSITE,appletv,🍎 Apple TV+
  - GEOSITE,youtube,📹 油管视频
  - GEOSITE,tiktok,🎵 TikTok
  - GEOSITE,bilibili,📺 哔哩哔哩
  - GEOSITE,ai,🤖 人工智能
  - GEOSITE,networktest,📈 网络测试
  - GEOSITE,proxy,🪜 代理域名
  - GEOSITE,cn,🔗 直连域名
```
② geosite-all-lite.dat 或 geosite-all-lite.db  
在 geosite-all.dat 和 geosite-all.db 的基础上去除了广告域名 `geosite:ads`，**有且仅有如下分类**：
```
  - GEOSITE,private,🔒 私有网络
  - GEOSITE,microsoft-cn,Ⓜ️ 微软服务
  - GEOSITE,apple-cn,🍎 苹果服务
  - GEOSITE,google-cn,📢 谷歌服务
  - GEOSITE,games-cn,🎮 游戏平台
  - GEOSITE,netflix,🎥 奈飞视频
  - GEOSITE,disney,📽️ 迪士尼+
  - GEOSITE,max,🎞️ Max
  - GEOSITE,primevideo,🎬 Prime Video
  - GEOSITE,appletv,🍎 Apple TV+
  - GEOSITE,youtube,📹 油管视频
  - GEOSITE,tiktok,🎵 TikTok
  - GEOSITE,bilibili,📺 哔哩哔哩
  - GEOSITE,ai,🤖 人工智能
  - GEOSITE,networktest,📈 网络测试
  - GEOSITE,proxy,🪜 代理域名
  - GEOSITE,cn,🔗 直连域名
```
③ geosite.dat 或 geosite.db  
在 geosite-all.dat 和 geosite-all.db 的基础上去除了流媒体和人工智能 `geosite:ai`，**有且仅有如下分类**：
```
  - GEOSITE,ads,🛑 广告拦截
  - GEOSITE,private,🔒 私有网络
  - GEOSITE,microsoft-cn,Ⓜ️ 微软服务
  - GEOSITE,apple-cn,🍎 苹果服务
  - GEOSITE,google-cn,📢 谷歌服务
  - GEOSITE,games-cn,🎮 游戏平台
  - GEOSITE,networktest,📈 网络测试
  - GEOSITE,proxy,🪜 代理域名
  - GEOSITE,cn,🔗 直连域名
```
④ geosite-lite.dat 或 geosite-lite.db  
在 geosite.dat 和 geosite.db 的基础上去除了广告域名 `geosite:ads`，包含的数据源最少，**有且仅有如下分类**：
```
  - GEOSITE,private,🔒 私有网络
  - GEOSITE,microsoft-cn,Ⓜ️ 微软服务
  - GEOSITE,apple-cn,🍎 苹果服务
  - GEOSITE,google-cn,📢 谷歌服务
  - GEOSITE,games-cn,🎮 游戏平台
  - GEOSITE,networktest,📈 网络测试
  - GEOSITE,proxy,🪜 代理域名
  - GEOSITE,cn,🔗 直连域名
```
⑤ Country-all.mmdb、geoip-all.dat、geoip-all.metadb 或 geoip-all.db  
源采用 [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip)，**包含但不限于如下分类**：
- 注：可[点此](https://github.com/Loyalsoldier/geoip/tree/release/text)查看包含的所有 IP 段列表
```
  - GEOIP,cloudflare,☁️ Cloudflare
  - GEOIP,cloudfront,🌐 CloudFront
  - GEOIP,facebook,👓 Facebook
  - GEOIP,fastly,🌎 Fastly
  - GEOIP,google,📢 谷歌
  - GEOIP,netflix,🎥 奈飞视频
  - GEOIP,telegram,📲 电报消息
  - GEOIP,twitter,✖️ Twitter
  - GEOIP,cn,🇨🇳 国内 IP
```
⑥ Country.mmdb、geoip.dat、geoip.metadb 或 geoip.db  
**有且仅有如下分类**：
```
  - GEOIP,netflix,🎥 奈飞视频
  - GEOIP,telegram,📲 电报消息
  - GEOIP,private,🔒 私有网络
  - GEOIP,cn,🇨🇳 国内 IP
```
⑦ Country-lite.mmdb、geoip-lite.dat、geoip-lite.metadb 或 geoip-lite.db  
在 Country.mmdb、geoip.dat、geoip.metadb 和 geoip.db 的基础上去除了流媒体，**有且仅有如下分类**：
```
  - GEOIP,telegram,📲 电报消息
  - GEOIP,private,🔒 私有网络
  - GEOIP,cn,🇨🇳 国内 IP
```
⑧ user.yaml（仅适用于 Clash）  
• `fake-ip-filter` 中添加[常用 fake-ip 地址过滤列表](https://github.com/juewuy/ShellCrash/blob/master/public/fake_ip_filter.list)，提高兼容性  
• `fake-ip-filter` 中添加 [TrackersList](https://github.com/XIU2/TrackersListCollection/all.txt)（udp 域名），防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition)无法连接 TrackersList UDP 协议  
<img src="https://user-images.githubusercontent.com/45238096/224113233-4d76dec2-495c-4790-a00e-538fc1469639.png" width="60%"/>  
• `fake-ip-filter` 中添加 AdGuardHome 相关域名，防止作为下游时检查更新和下载“DNS 黑名单”失败：
```
    - 'static.adtidy.org'
    - 'adguardteam.github.io'
    - 'anti-ad.net'
```
• 若想自己生成配置文件 user.yaml，可以 [Fork 本项目](https://github.com/DustinWin/ruleset_geox/fork)后编辑 *.github/workflows/build-clash-ruleset_geox.yml* 文件内的 `name: Generate xxx-user.yaml` 部分  
• 若 DNS 模式选用的是 `redir-host`，必须进行 DNS 分流（可以参考[Clash.Meta 内核 DNS 分流教程](https://github.com/DustinWin/clash_singbox-tutorials/tree/main/%E6%95%99%E7%A8%8B%E5%90%88%E9%9B%86/%E8%BF%9B%E9%98%B6%E7%AF%87)），可以进入 *.github/workflows/build-clash-ruleset_geox.yml* 文件，编辑 `Generate xxx-redir-host-user.yaml` 部分，将 `nameserver` 中的 `🪜 代理域名`改成可以访问外网的策略组名称，或者直接将 `'https://dns.google/dns-query#🪜 代理域名'` 修改为 `'tls://dns.google'`
# 二、 文件下载（以 geosite.dat、geosite.db、Country.mmdb、geoip.dat、geoip.metadb 和 geoip.db 为例）
## 1. Clash GeoX 规则集文件下载
① geosite.dat  
• GitHub 源：https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geox/geosite.dat  
• jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/geosite.dat  
• GitHub Proxy 源：https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geox/geosite.dat  
② Country.mmdb  
• GitHub 源：https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geox/Country.mmdb  
• jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/Country.mmdb  
• GitHub Proxy 源：https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geox/Country.mmdb  
③ geoip.dat  
• GitHub 源：https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geox/geoip.dat  
• jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/geoip.dat  
• GitHub Proxy 源：https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geox/geoip.dat  
④ geoip.metadb  
• GitHub 源：https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geox/geoip.metadb  
• jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/geoip.metadb  
• GitHub Proxy 源：https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geox/geoip.metadb
## 2. sing-box 规则集文件下载
① geosite.db  
• GitHub 源：https://raw.githubusercontent.com/DustinWin/ruleset_geox/sing-box/geox/geosite.db  
• jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@sing-box/geox/geosite.db  
• GitHub Proxy 源：https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geox/sing-box/geox/geosite.db
② geoip.db  
• GitHub 源：https://raw.githubusercontent.com/DustinWin/ruleset_geox/sing-box/geox/geoip.db  
• jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@sing-box/geox/geoip.db  
• GitHub Proxy 源：https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geox/sing-box/geox/geoip.db
# 三、 文件导入（以 [ShellClash](https://github.com/juewuy/ShellCrash) 使用 Clash.Meta 内核导入 geosite.dat、Country.mmdb、geoip.dat 和 geoip.metadb 为例）
## 1. DNS 模式为 `fake-ip`  
连接 SSH 后执行如下命令：
```
curl -o $CRASHDIR/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/geosite.dat
curl -o $CRASHDIR/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/Country.mmdb
curl -o $CRASHDIR/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/geoip.dat
curl -o $CRASHDIR/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/fake-ip-user.yaml
$CRASHDIR/start.sh restart
```
## 2. DNS 模式为 `redir-host`  
连接 SSH 后执行如下命令：
```
curl -o $CRASHDIR/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/geosite.dat
curl -o $CRASHDIR/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/Country.mmdb
curl -o $CRASHDIR/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/geoip.dat
curl -o $CRASHDIR/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/redir-host-user.yaml
$CRASHDIR/start.sh restart
```
# 四、 添加定时任务（以 ShellClash 为例）
1. 连接 SSH 后运行 `vi $CRASHDIR/task/task.user`，按一下 Ins 键（Insert 键），粘贴如下内容：
```
201#curl -o /data/clash/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/geosite.dat && curl -o /data/clash/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geoip@release/Country.mmdb && curl -o /data/clash/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/geoip.dat &&  && /data/clash/start.sh restart >/dev/null 2>&1#更新GeoX路由规则文件
202#curl -o /data/clash/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/fake-ip-user.yaml && /data/clash/start.sh restart >/dev/null 2>&1#更新user.yaml
```
2. 按一下 Esc 键（退出键），输入英文冒号`:`，继续输入 `wq` 并回车
3. 执行 `crash`，进入 ShellClash->5 配置自动任务->1 添加自动任务，可以看到末尾就有添加的定时任务，输入对应的数字并回车后可设置执行条件  
**改天继续写 rule-set 部分**

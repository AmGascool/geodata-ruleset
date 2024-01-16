# 一、 GeoX 规则集文件说明
## 1. 文件类型
① [Clash](https://github.com/Dreamacro/clash) GeoX 规则集文件，包括：geosite.dat、Country.mmdb、geoip.dat 和 geoip.metadb（仅限 [Clash.Meta 内核](https://github.com/MetaCubeX/mihomo)）等  
② [sing-box](https://github.com/SagerNet/sing-box) GeoX 规则集文件，包括：geosite.db 和 geoip.db 等
## 2. 数据源
① 每天凌晨 3 点（北京时间）自动构建，根据 [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat) 和 [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip) 进行深度定制，可点击查看包含的[域名列表](https://github.com/DustinWin/ruleset_geox/tree/master/Domains)和 [IP 段列表](https://github.com/DustinWin/ruleset_geox/tree/master/IPs)  
② `geosite,ads,🛑 广告拦截` 源采用 [privacy-protection-tools/anti-AD](https://github.com/privacy-protection-tools/anti-AD)  
③ `geosite,private,🔒 私有网络` 源采用 [v2fly/domain-list-community/private](https://github.com/v2fly/domain-list-community/blob/master/data/private) 和 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan) 组合，并添加主流 [Clash dashboard 在线面板](https://github.com/DustinWin/clash_singbox-tools/tree/main/Clash-dashboard)域名（`clash.razord.top`、`clash.metacubex.one`、`yacd.haishan.me`、`yacd.metacubex.one` 和 `d.metacubex.one`）  
④ `geosite,microsoft-cn,Ⓜ️ 微软服务` 源采用 [v2fly/domain-list-community/microsoft@cn](https://github.com/v2fly/domain-list-community/blob/master/data/microsoft)  
⑤ `geosite,apple-cn,🍎 苹果服务` 源采用 [felixonmars/dnsmasq-china-list/apple.china.conf](https://github.com/felixonmars/dnsmasq-china-list)  
⑥ `geosite,google-cn,📢 谷歌服务` 源采用 [felixonmars/dnsmasq-china-list/google.china.conf](https://github.com/felixonmars/dnsmasq-china-list)  
⑦ `geosite,games-cn,🎮 游戏平台` 源采用 [v2fly/domain-list-community/category-games@cn](https://github.com/v2fly/domain-list-community/blob/master/data/category-games)、[blackmatrix7/ios_rule_script/SteamCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/SteamCN) 和 [blackmatrix7/ios_rule_script/GameDownloadCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Game/GameDownloadCN) 组合  
⑧ `geosite,netflix,🎥 奈飞视频` 源采用 [blackmatrix7/ios_rule_script/Netflix](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)  
⑨ `geosite,disney,📽️ 迪士尼+` 源采用 [blackmatrix7/ios_rule_script/Disney](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Disney)  
⑩ `geosite,max,🎞️ Max` 源采用 [blackmatrix7/ios_rule_script/HBO](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/HBO)  
⑪ `geosite,primevideo,🎬 Prime Video` 源采用 [blackmatrix7/ios_rule_script/PrimeVideo](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/PrimeVideo)  
⑫ `geosite,appletv,🍎 Apple TV+` 源采用 [blackmatrix7/ios_rule_script/AppleTV](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/AppleTV)  
⑬ `geosite,youtube,📹 油管视频` 源采用 [blackmatrix7/ios_rule_script/YouTube](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/YouTube)  
⑭ `geosite,tiktok,🎵 TikTok` 源采用 [blackmatrix7/ios_rule_script/TikTok](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/TikTok)  
⑮ `geosite,bilibili,📺 哔哩哔哩` 源采用 [blackmatrix7/ios_rule_script/BiliBili](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/BiliBili)  
⑯ `geosite,ai,🤖 人工智能` 源采用 [blackmatrix7/ios_rule_script/OpenAI](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/OpenAI)、[blackmatrix7/ios_rule_script/Bing](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Bing) 和 [blackmatrix7/ios_rule_script/BardAI](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/BardAI) 组合  
⑰ `geosite,networktest,📈 网络测试` 源采用 [blackmatrix7/ios_rule_script/Speedtest](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Speedtest) 和 IPv6 测试域名关键字（`keyword`，包括：`ipv6-test`、`test-ipv6`、`ipv6test` 和 `testipv6`）组合    
⑱ `geosite,proxy,🪜 代理域名` 源采用 [cokebar/gfwlist2dnsmasq](https://github.com/cokebar/gfwlist2dnsmasq) 生成的 [gfwlist](https://github.com/gfwlist/gfwlist) 和 [Loyalsoldier/domain-list-custom/geolocation-!cn.txt](https://github.com/Loyalsoldier/domain-list-custom) 组合  
⑲ `geosite,cn,🔗 直连域名` 源采用 [blackmatrix7/ios_rule_script/ChinaMax](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)，添加 `static.adtidy.org` 域名，防止 [AdGuardHome](https://github.com/AdguardTeam/AdGuardHome) 作为 Clash 下游时检查更新失败（在 Clash 中必须使用国内 DNS 对其进行解析）  
⑳ `geoip,netflix,🎥 奈飞视频` 源采用 [blackmatrix7/ios_rule_script/Netflix/Netflix_IP.txt](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)  
㉑ `geoip,telegram,📲 电报消息` 源采用 [Telegram IP 段](https://core.telegram.org/resources/cidr.txt)  
㉒ `geoip,private,🔒 私有网络` 源采用 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)  
㉓ `geoip,cn,🇨🇳 国内 IP` 源采用 [GeoLite2/cn.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[17mon/china_ip_list](https://github.com/17mon/china_ip_list)、[gaoyifan/china-operator-ip](https://github.com/gaoyifan/china-operator-ip) 和 [blackmatrix7/ios_rule_script/ChinaIPs/ChinaIPs_IP.txt](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaIPs) 组合  
**规则名称与规则集文件的对应关系如下表：**
|文件名称|包含规则|
|-----|-----|
|geosite-all.dat 和 geosite-all.db|`ads`、`private`、`microsoft-cn`、`apple-cn`、`google-cn`、`games-cn`、`netflix`、`disney`、`max`、`primevideo`、`appletv`、`youtube`、`tiktok`、`bilibili`、`ai`、`networktest`、`proxy` 和 `cn`|
|geosite-all-lite.dat 和 geosite-all-lite.db|~~`ads`~~、`private`、`microsoft-cn`、`apple-cn`、`google-cn`、`games-cn`、`netflix`、`disney`、`max`、`primevideo`、`appletv`、`youtube`、`tiktok`、`bilibili`、`ai`、`networktest`、`proxy` 和 `cn`|
|geosite.dat 和 geosite.db|`ads`、`private`、`microsoft-cn`、`apple-cn`、`google-cn`、`games-cn`、`networktest`、`proxy` 和 `cn`|
|geosite-lite.dat 和 geosite-lite.db|~~`ads`~~、`private`、`microsoft-cn`、`apple-cn`、`google-cn`、`games-cn`、`networktest`、`proxy` 和 `cn`|
|Country-all.mmdb、geoip-all.dat、geoip-all.metadb 和 geoip-all.db|来源于 [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip)，[点此查看](https://github.com/Loyalsoldier/geoip/tree/release/text)|
|Country.mmdb、geoip.dat、geoip.metadb 和 geoip.db|`netflix`、`telegram`、`private` 和 `cn`|
|Country-lite.mmdb、geoip-lite.dat、geoip-lite.metadb 和 geoip-lite.db|~~`netflix`~~、`telegram`、`private` 和 `cn`|
## 3. 文件下载（以 geosite.dat、geosite.db、Country.mmdb、geoip.dat、geoip.metadb 和 geoip.db 为例）
<table>
  <tr>
    <td rowspan="3">geosite.dat</td>
    <td>GitHub 源：https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geosite.dat</td>
  </tr>
  <tr>
    <td>jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geosite.dat</td>
  </tr>
  <tr>
    <td>GitHub Proxy 源：https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geosite.dat</td>
  </tr>
  <tr>
    <td rowspan="3">geosite.db</td>
    <td>GitHub 源：https://raw.githubusercontent.com/DustinWin/ruleset_geox/sing-box/geosite.db</td>
  </tr>
  <tr>
    <td>jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@sing-box/geosite.db</td>
  </tr>
  <tr>
    <td>GitHub Proxy 源：https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geox/sing-box/geosite.db</td>
  </tr>
  <tr>
    <td rowspan="3">Country.mmdb</td>
    <td>GitHub 源：https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/Country.mmdb</td>
  </tr>
  <tr>
    <td>jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/Country.mmdb</td>
  </tr>
  <tr>
    <td>GitHub Proxy 源：https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/Country.mmdb</td>
  </tr>
  <tr>
    <td rowspan="3">geoip.dat</td>
    <td>GitHub 源：https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geoip.dat</td>
  </tr>
  <tr>
    <td>jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geoip.dat</td>
  </tr>
  <tr>
    <td>GitHub Proxy 源：https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geoip.dat</td>
  </tr>
  <tr>
    <td rowspan="3">geoip.metadb</td>
    <td>GitHub 源：https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geoip.metadb</td>
  </tr>
  <tr>
    <td>jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geoip.metadb</td>
  </tr>
  <tr>
    <td>GitHub Proxy 源：https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geox/clash/geoip.metadb</td>
  </tr>
  <tr>
    <td rowspan="3">geoip.db</td>
    <td>GitHub 源：https://raw.githubusercontent.com/DustinWin/ruleset_geox/sing-box/geoip.db</td>
  </tr>
  <tr>
    <td>jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@sing-box/geoip.db</td>
  </tr>
  <tr>
    <td>GitHub Proxy 源：https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geox/sing-box/geoip.db</td>
  </tr>
</table>

## 4. 文件导入
① 导入到 Linux 端（以 [ShellClash](https://github.com/juewuy/ShellCrash) 导入 geosite.dat、geosite.db、Country.mmdb、geoip.dat、geoip.metadb 和 geoip.db 为例） 
连接 SSH 后执行如下命令：
```
# Clash 内核
curl -o $CRASHDIR/geosite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geosite.dat
curl -o $CRASHDIR/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/Country.mmdb
curl -o $CRASHDIR/geoip.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geoip.dat
# Clash.Meta 内核
curl -o $CRASHDIR/geoip.metadb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geoip.metadb
# sing-box 内核
curl -o $CRASHDIR/geosite.db -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@sing-box/geosite.db
curl -o $CRASHDIR/geoip.db -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@sing-box/geoip.db
$CRASHDIR/start.sh restart
```
② 导入到 Windows 端（以 [Clash Verge](https://github.com/MetaCubeX/clash-verge) 导入 geosite.dat、Country.mmdb、geoip.dat 和 geoip.metadb 为例）  
以管理员身份运行 CMD，执行如下命令：
```
taskkill /f /t /im "Clash Verge*"
taskkill /f /t /im Clash-Verge*
taskkill /f /t /im clash-meta*
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geosite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geosite.dat
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/Country.mmdb
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geoip.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geoip.dat
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geoip.metadb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geoip.metadb
pause
```
## 5. 文件拓展
## 1. user.yaml（仅限 Clash.Meta 内核）
① `fake-ip-filter` 中添加[常用 fake-ip 地址过滤列表](https://github.com/juewuy/ShellCrash/blob/master/public/fake_ip_filter.list)，提高兼容性  
② `fake-ip-filter` 中添加 [TrackersList](https://github.com/XIU2/TrackersListCollection/all.txt)（udp 域名），防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition)无法连接 TrackersList UDP 协议  
<img src="https://user-images.githubusercontent.com/45238096/224113233-4d76dec2-495c-4790-a00e-538fc1469639.png" width="60%"/>  
③ `fake-ip-filter` 中添加 AdGuardHome 相关域名（包括：`static.adtidy.org`、`adguardteam.github.io` 和 `anti-ad.net`），防止作为下游时检查更新和下载“DNS 黑名单”失败  
④ 若想自己生成配置文件 user.yaml，可以 [Fork 本项目](https://github.com/DustinWin/ruleset_geox/fork)后编辑 *.github/workflows/build.yml* 文件内的 `name: Generate geox-xxx-user.yaml` 部分  
⑤ 若 DNS 模式选用的是 `redir-host`，必须进行 DNS 分流（可以参考[Clash.Meta 内核 DNS 分流教程](https://github.com/DustinWin/clash_singbox-tutorials/tree/main/%E6%95%99%E7%A8%8B%E5%90%88%E9%9B%86/%E8%BF%9B%E9%98%B6%E7%AF%87)），可以进入 *.github/workflows/build.yml* 文件，编辑 `Generate geox-redirhost-user.yaml` 部分，将 `nameserver` 中的 `🪜 代理域名`改成可以访问外网的策略组名称，或者直接将 `'https://dns.google/dns-query#🪜 代理域名'` 修改为 `'tls://dns.google'`  
⑥ 导入 Linux 端（以导入 ShellClash 为例）  
• 将下面命令中的`{DNS 模式}`替换为正在使用的 DNS 模式（`fakeip` 或 `redirhost`）  
• 连接 SSH 后执行如下命令：
```
curl -o $CRASHDIR/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox-{DNS 模式}-user.yaml
$CRASHDIR/start.sh restart
```
⑦ 导入 Windows 端（以导入 Clash Verge 为例）
• 首次使用可进入 Clash Verge->订阅，新建“Merge”类型的配置，完成后点击“保存”，右击新建的 Merge 文件，选择“启用”  
• 进入文件夹 *%APPDATA%\io.github.clash-verge-rev.clash-verge-rev\profiles*，找到与上一步新建的 Merge 文件相对应的 .yaml 文件，复制其文件名并替换下面命令中的`{文件名}`
• 将下面命令中的`{DNS 模式}`替换为正在使用的 DNS 模式（`fakeip` 或 `redirhost`）  
• 以管理员身份打开 CMD 命令提示符，执行如下命令：
```
taskkill /f /t /im "Clash Verge*"
taskkill /f /t /im Clash-Verge*
taskkill /f /t /im clash-meta*
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\profiles\{文件名}.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox-{DNS 模式}-user.yaml
```
## 2. 添加定时任务（以 ShellClash 为例）
① 连接 SSH 后运行 `vi $CRASHDIR/task/task.user`，按一下 Ins 键（Insert 键），粘贴如下内容：
```
# Clash 内核
201#curl -o /data/ShellCrash/geosite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geosite.dat && curl -o /data/ShellCrash/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/Country.mmdb && curl -o /data/ShellCrash/geoip.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geoip.dat &&  && /data/clash/start.sh restart >/dev/null 2>&1#更新GeoX路由规则文件
202#curl -o /data/clash/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geox@clash/geox/fake-ip-user.yaml && /data/clash/start.sh restart >/dev/null 2>&1#更新user.yaml
```
2. 按一下 Esc 键（退出键），输入英文冒号`:`，继续输入 `wq` 并回车
3. 执行 `crash`，进入 ShellClash->5 配置自动任务->1 添加自动任务，可以看到末尾就有添加的定时任务，输入对应的数字并回车后可设置执行条件  
**改天继续写 rule-set 部分**


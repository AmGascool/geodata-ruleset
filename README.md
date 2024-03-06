# 一、 geodata 规则集文件说明
## 1. 文件类型
① [Clash](https://github.com/Dreamacro/clash) geodata 规则集文件，包括：geosite.dat、geoip.dat、Country.mmdb 和 geoip.metadb（仅限 [mihomo 内核](https://github.com/MetaCubeX/mihomo)）等  
② [sing-box](https://github.com/SagerNet/sing-box) geodata 规则集文件，包括：geosite.db 和 geoip.db 等
## 2. 数据源
① 每天凌晨 3 点（北京时间）自动构建，根据 [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat) 和 [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip) 进行深度定制，可点击查看包含的[域名列表](https://github.com/DustinWin/ruleset_geodata/tree/domains)和 [IP 段列表](https://github.com/DustinWin/ruleset_geodata/tree/ips)  
② `geosite,ads,🛑 广告拦截` 源采用 [privacy-protection-tools/anti-AD](https://github.com/privacy-protection-tools/anti-AD)  
③ `geosite,private,🔒 私有网络` 源采用 [v2fly/domain-list-community/private](https://github.com/v2fly/domain-list-community/blob/master/data/private) 和 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（仅域名）组合，并添加主流 [Clash dashboard 在线面板](https://github.com/DustinWin/clash_singbox-tools/tree/main/Clash-dashboard)域名（`clash.razord.top`、`clash.metacubex.one`、`yacd.haishan.me`、`yacd.metacubex.one` 和 `d.metacubex.one`）  
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
⑰ `geosite,networktest,📈 网络测试` 源采用 [v2fly/domain-list-community/speedtest](https://github.com/v2fly/domain-list-community/blob/master/data/speedtest)、[blackmatrix7/ios_rule_script/Speedtest](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Speedtest) 和 IPv6 测试域名关键字（`keyword`，包括：`ipv6-test`、`test-ipv6`、`ipv6test` 和 `testipv6`）组合    
⑱ `geosite,proxy,🪜 代理域名` 源采用 [cokebar/gfwlist2dnsmasq](https://github.com/cokebar/gfwlist2dnsmasq) 生成的 [gfwlist](https://github.com/gfwlist/gfwlist)、[Loyalsoldier/domain-list-custom/geolocation-!cn.txt](https://github.com/Loyalsoldier/domain-list-custom) 和 [blackmatrix7/ios_rule_script/Global](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Global) 组合  
⑲ `geosite,cn,🔗 直连域名` 源采用 [Loyalsoldier/domain-list-custom/cn.txt](https://github.com/Loyalsoldier/domain-list-custom) 和 [blackmatrix7/ios_rule_script/ChinaMax](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)（仅域名）  
⑳ `geoip,netflix,🎥 奈飞视频` 源采用 [GeoLite2/netflix.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) 和 [blackmatrix7/ios_rule_script/Netflix](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix) 组合  
㉑ `geoip,telegram,📲 电报消息` 源采用 [GeoLite2/telegram.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[Telegram IP 段](https://core.telegram.org/resources/cidr.txt) 和 [blackmatrix7/ios_rule_script/Telegram](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Telegram)（仅 IP）组合  
㉒ `geoip,private,🔒 私有网络` 源采用 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（仅 IP）  
㉓ `geoip,cn,🇨🇳 国内 IP` 源采用 [GeoLite2/cn.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[17mon/china_ip_list](https://github.com/17mon/china_ip_list)、[gaoyifan/china-operator-ip](https://github.com/gaoyifan/china-operator-ip) 和 [blackmatrix7/ios_rule_script/ChinaIPs](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaIPs) 组合
## 3. 文件下载
**规则集文件包含的规则和下载地址对应关系如下表：**
<table>
  <tr>
    <td><b>规则集文件名称</b></td>
    <td align="center"><b>包含规则</b></td>
    <td><b>GitHub 源</b></td>
    <td><b>jsDelivr 源</b></td>
    <td><b>GitHub Proxy 源</b></td>
  </tr>
  <tr>
    <td>geosite-all.dat</td>
    <td rowspan="2"><code>ads</code>、<code>private</code>、<code>microsoft-cn</code>、<code>apple-cn</code>、<code>google-cn</code>、<code>games-cn</code>、<code>netflix</code>、<code>disney</code>、<code>max</code>、<code>primevideo</code>、<code>appletv</code>、<code>youtube</code>、<code>tiktok</code>、<code>bilibili</code>、<code>ai</code>、<code>networktest</code>、<code>proxy</code> 和 <code>cn</code></td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geosite-all.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite-all.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geosite-all.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite-all.db</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geosite-all.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geosite-all.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geosite-all.db">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite-all-lite.dat</td>
    <td rowspan="2"><del><code>ads</code></del>、<code>private</code>、<code>microsoft-cn</code>、<code>apple-cn</code>、<code>google-cn</code>、<code>games-cn</code>、<code>netflix</code>、<code>disney</code>、<code>max</code>、<code>primevideo</code>、<code>appletv</code>、<code>youtube</code>、<code>tiktok</code>、<code>bilibili</code>、<code>ai</code>、<code>networktest</code>、<code>proxy</code> 和 <code>cn</code></td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geosite-all-lite.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite-all-lite.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geosite-all-lite.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite-all-lite.db</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geosite-all-lite.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geosite-all-lite.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geosite-all-lite.db">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite.dat</td>
    <td rowspan="2"><code>ads</code>、<code>private</code>、<code>microsoft-cn</code>、<code>apple-cn</code>、<code>google-cn</code>、<code>games-cn</code>、<code>networktest</code>、<code>proxy</code> 和 <code>cn</code></td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geosite.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geosite.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite.db</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geosite.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geosite.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geosite.db">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite-lite.dat</td>
    <td rowspan="2"><del><code>ads</code></del>、<code>private</code>、<code>microsoft-cn</code>、<code>apple-cn</code>、<code>google-cn</code>、<code>games-cn</code>、<code>networktest</code>、<code>proxy</code> 和 <code>cn</code></td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geosite-lite.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite-lite.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geosite-lite.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite-lite.db</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geosite-lite.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geosite-lite.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geosite-lite.db">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-all.dat</td>
    <td rowspan="4" align="center"><a href="https://github.com/Loyalsoldier/geoip/tree/release/text">点此查看</a></td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geoip-all.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip-all.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geoip-all.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-all.mmdb</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/Country-all.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country-all.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/Country-all.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-all.metadb</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geoip-all.metadb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip-all.metadb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geoip-all.metadb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-all.db</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geoip-all.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geoip-all.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geoip-all.db">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip.dat</td>
    <td rowspan="4"><code>netflix</code>、<code>telegram</code>、<code>private</code> 和 <code>cn</code></td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geoip.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geoip.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>Country.mmdb</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/Country.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/Country.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip.metadb</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geoip.metadb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.metadb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geoip.metadb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip.db</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geoip.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geoip.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geoip.db">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-lite.dat</td>
    <td rowspan="4"><del><code>netflix</code></del>、<code>telegram</code>、<code>private</code> 和 <code>cn</code></td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geoip-lite.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip-lite.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geoip-lite.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-lite.mmdb</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/Country-lite.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country-lite.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/Country-lite.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-lite.metadb</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geoip-lite.metadb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip-lite.metadb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/clash/geoip-lite.metadb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-lite.db</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geoip-lite.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geoip-lite.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/ruleset_geodata/sing-box/geoip-lite.db">点此下载</a></td>
  </tr>
</table>

## 4. 文件导入
### ① 导入到 Linux 端（以 [ShellCrash](https://github.com/juewuy/ShellCrash) 导入 geosite.dat、geosite.db、geoip.dat、Country.mmdb、geoip.metadb 和 geoip.db 为例）
连接 SSH 后执行如下命令：
```
# 适用于 Clash 内核
curl -o $CRASHDIR/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite.dat
curl -o $CRASHDIR/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.dat
curl -o $CRASHDIR/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country.mmdb
# 适用于 mihomo 内核
curl -o $CRASHDIR/geoip.metadb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.metadb
# 适用于 sing-box 内核
curl -o $CRASHDIR/geosite.db -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geosite.db
curl -o $CRASHDIR/geoip.db -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geoip.db
$CRASHDIR/start.sh restart
```
### ② 导入到 Windows 端（以 [Clash Verge](https://github.com/clash-verge-rev/clash-verge-rev) 导入 geosite.dat、geoip.dat、Country.mmdb和 geoip.metadb 为例）
以管理员身份运行 CMD 命令提示符，执行如下命令：
```
taskkill /f /t /im "Clash Verge*"
taskkill /f /t /im Clash-Verge*
taskkill /f /t /im clash-meta*
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geosite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite.dat
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geoip.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.dat
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country.mmdb
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geoip.metadb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.metadb
```
## 5. 文件拓展
### ① [user.yaml](https://github.com/DustinWin/ruleset_geodata/tree/clash-config)（仅限 mihomo 内核）
- 注：含有“fakeip”字样的 .yaml 配置文件中才含有 `fake-ip-filter` 参数

**配置文件名关键字与使用场景对应关系如下表：**
|文件名关键字|使用场景|
|-----|-----|
|lite|无广告拦截，搭配 AdGuardHome|
|noprocess|不含进程匹配模式，仅适合 ShellCrash|

• `fake-ip-filter` 参数  
`fake-ip-filter` 中添加[常用 fake-ip 地址过滤列表](https://github.com/juewuy/ShellCrash/blob/master/public/fake_ip_filter.list)，提高兼容性  
`fake-ip-filter` 中添加 [TrackersList](https://github.com/XIU2/TrackersListCollection/blob/master/all.txt)（udp 域名），防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition)无法连接 TrackersList UDP 协议  
<img src="https://user-images.githubusercontent.com/45238096/224113233-4d76dec2-495c-4790-a00e-538fc1469639.png" width="60%"/>  
`fake-ip-filter` 中添加 AdGuardHome 相关域名（包括：`adguardteam.github.io`、`adrules.top`、`anti-ad.net` 和 `static.adtidy.org`），防止作为下游时检查更新和下载“DNS 黑名单”失败  
若想自己生成配置文件 user.yaml，可以 [Fork 本项目](https://github.com/DustinWin/ruleset_geodata/fork)后编辑 *.github/workflows/build.yml* 文件内的 ```name: Generate `clash` geodata-xxx-user.yaml``` 部分  
若 DNS 模式选用的是 `redir-host`，必须进行 DNS 分流（可以参考 [mihomo 内核 DNS 分流教程](https://github.com/DustinWin/clash_singbox-tutorials/tree/main/%E6%95%99%E7%A8%8B%E5%90%88%E9%9B%86/Clash/%E8%BF%9B%E9%98%B6%E7%AF%87)），可以进入 *.github/workflows/build.yml* 文件，编辑 ```Generate `clash` geodata-redirhost-user.yaml``` 部分，将 `nameserver` 中的 `🪜 代理域名` 改成可以访问外网的策略组名称，或者直接将 `'https://dns.google/dns-query#🪜 代理域名'` 修改为 `'tls://dns.google'`  
• 导入 Linux 端（以导入 ShellCrash 为例）  
将下面命令中的 `{DNS 模式}` 替换为正在使用的 DNS 模式（`fakeip` 或 `redirhost`）  
连接 SSH 后执行如下命令：
```
curl -o $CRASHDIR/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-config/geodata-{DNS 模式}-user-lite-noprocess.yaml
$CRASHDIR/start.sh restart
```
• 导入 Windows 端（以导入 Clash Verge 为例）  
首次使用可进入 Clash Verge->订阅，新建“Merge”类型的配置，完成后点击“保存”，右击新建的 Merge 文件，点击“启用”  
进入文件夹 *%APPDATA%\io.github.clash-verge-rev.clash-verge-rev\profiles*，找到与上一步新建的 Merge 文件相对应的 .yaml 文件，复制其文件名并替换下面命令中的 `{Merge 文件名}`  
将下面命令中的 `{DNS 模式}` 替换为正在使用的 DNS 模式（`fakeip` 或 `redirhost`）  
以管理员身份打开 CMD 命令提示符，执行如下命令：
```
taskkill /f /t /im "Clash Verge*"
taskkill /f /t /im Clash-Verge*
taskkill /f /t /im clash-meta*
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\profiles\{Merge 文件名}.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-config/geodata-{DNS 模式}-user.yaml
```
### ② [dns.json](https://github.com/DustinWin/ruleset_geodata/tree/sing-box-config)（仅限 sing-box PuerNya 版内核）
- 注：含有“lite”后缀的 .json 配置文件适合无 sing-box 广告拦截且配合 [AdGuardHome](https://github.com/AdguardTeam/AdGuardHome) 的方案

• `dns.rules` 数组  
`dns.rules` 中添加 AdGuardHome 相关域名（包括：`adguardteam.github.io`、`adrules.top`、`anti-ad.net` 和 `static.adtidy.org`），防止作为下游时检查更新和下载“DNS 黑名单”失败  
• 导入 Linux 端（以导入 ShellCrash 为例）   
连接 SSH 后执行如下命令：
```
curl -o $CRASHDIR/jsons/dns.json -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-config/geodata-dns-lite.json
$CRASHDIR/start.sh restart
```
### ③ 添加定时任务（以 ShellCrash 为例，安装路径为 */data/ShellCrash*）
连接 SSH 后执行 `vi $CRASHDIR/task/task.user`，按一下 Ins 键（Insert 键），粘贴如下内容：
```
# 适用于 Clash 内核
201#curl -o /data/ShellCrash/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite.dat && curl -o /data/ShellCrash/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.dat && curl -o /data/ShellCrash/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country.mmdb && /data/ShellCrash/start.sh restart >/dev/null 2>&1#更新geodata路由规则文件
# 适用于 mihomo 内核
202#curl -o /data/ShellCrash/geoip.metadb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.metadb && /data/ShellCrash/start.sh restart >/dev/null 2>&1#更新geodata路由规则文件
203#curl -o /data/ShellCrash/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-config/geodata-{DNS 模式}-user-lite-noprocess.yaml && /data/ShellCrash/start.sh restart >/dev/null 2>&1#更新user.yaml
# 适用于 sing-box 内核
204#curl -o /data/ShellCrash/geosite.db -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite.db && curl -o /data/ShellCrash/geoip.db -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.db && /data/ShellCrash/start.sh restart >/dev/null 2>&1#更新geodata路由规则文件
```
按一下 Esc 键（退出键），输入英文冒号 `:`，继续输入 `wq` 并回车  
执行 `crash`，进入 ShellCrash->5 配置自动任务->1 添加自动任务，可以看到末尾就有添加的定时任务，输入对应的数字并回车后可设置执行条件
# 二、 ruleset 规则集文件说明
## 1. 文件类型
① Clash ruleset 规则集文件，格式为 `.yaml`（`format: text`）  
② sing-box ruleset 规则集文件，格式有 `.json`（`"format": "source"`）和 `.srs`（`"format": "binary"`）
## 2. 数据源
① 每天凌晨 3 点（北京时间）自动构建  
② `rule-set,ads,🛑 广告拦截` 源采用 [privacy-protection-tools/anti-AD](https://github.com/privacy-protection-tools/anti-AD)  
③ `rule-set,applications,🖥️ 直连软件` 源采用 [Loyalsoldier/clash-rules/applications.txt](https://github.com/Loyalsoldier/clash-rules)  
④ `rule-set,private,🔒 私有网络` 源采用 [v2fly/domain-list-community/private](https://github.com/v2fly/domain-list-community/blob/master/data/private) 和 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（仅域名）组合，并添加主流 [Clash dashboard 在线面板](https://github.com/DustinWin/clash_singbox-tools/tree/main/Clash-dashboard)域名（`clash.razord.top`、`clash.metacubex.one`、`yacd.haishan.me`、`yacd.metacubex.one` 和 `d.metacubex.one`）  
⑤ `rule-set,microsoft-cn,Ⓜ️ 微软服务` 源采用 [v2fly/domain-list-community/microsoft@cn](https://github.com/v2fly/domain-list-community/blob/master/data/microsoft)  
⑥ `rule-set,apple-cn,🍎 苹果服务` 源采用 [felixonmars/dnsmasq-china-list/apple.china.conf](https://github.com/felixonmars/dnsmasq-china-list)  
⑦ `rule-set,google-cn,📢 谷歌服务` 源采用 [felixonmars/dnsmasq-china-list/google.china.conf](https://github.com/felixonmars/dnsmasq-china-list)  
⑧ `rule-set,games-cn,🎮 游戏平台` 源采用 [v2fly/domain-list-community/category-games@cn](https://github.com/v2fly/domain-list-community/blob/master/data/category-games)、[blackmatrix7/ios_rule_script/SteamCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/SteamCN) 和 [blackmatrix7/ios_rule_script/GameDownloadCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Game/GameDownloadCN) 组合  
⑨ `rule-set,netflix,🎥 奈飞视频` 源采用 [blackmatrix7/ios_rule_script/Netflix](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)（仅域名）  
⑩ `rule-set,disney,📽️ 迪士尼+` 源采用 [blackmatrix7/ios_rule_script/Disney](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Disney)  
⑪ `rule-set,max,🎞️ Max` 源采用 [blackmatrix7/ios_rule_script/HBO](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/HBO)  
⑫ `rule-set,primevideo,🎬 Prime Video` 源采用 [blackmatrix7/ios_rule_script/PrimeVideo](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/PrimeVideo)  
⑬ `rule-set,appletv,🍎 Apple TV+` 源采用 [blackmatrix7/ios_rule_script/AppleTV](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/AppleTV)  
⑭ `rule-set,youtube,📹 油管视频` 源采用 [blackmatrix7/ios_rule_script/YouTube](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/YouTube)  
⑮ `rule-set,tiktok,🎵 TikTok` 源采用 [blackmatrix7/ios_rule_script/TikTok](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/TikTok)  
⑯ `rule-set,bilibili,📺 哔哩哔哩` 源采用 [blackmatrix7/ios_rule_script/BiliBili](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/BiliBili)  
⑰ `rule-set,ai,🤖 人工智能` 源采用 [blackmatrix7/ios_rule_script/OpenAI](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/OpenAI)、[blackmatrix7/ios_rule_script/Bing](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Bing) 和 [blackmatrix7/ios_rule_script/BardAI](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/BardAI) 组合  
⑱ `rule-set,networktest,📈 网络测试` 源采用 [v2fly/domain-list-community/speedtest](https://github.com/v2fly/domain-list-community/blob/master/data/speedtest)、[blackmatrix7/ios_rule_script/Speedtest](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Speedtest) 和 IPv6 测试域名关键字（`keyword`，包括：`ipv6-test`、`test-ipv6`、`ipv6test` 和 `testipv6`）组合  
⑲ `rule-set,proxy,🪜 代理域名` 源采用 [cokebar/gfwlist2dnsmasq](https://github.com/cokebar/gfwlist2dnsmasq) 生成的 [gfwlist](https://github.com/gfwlist/gfwlist)、[Loyalsoldier/domain-list-custom/geolocation-!cn.txt](https://github.com/Loyalsoldier/domain-list-custom) 和 [blackmatrix7/ios_rule_script/Global](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Global) 组合  
⑳ `rule-set,cn,🔗 直连域名` 源采用 [Loyalsoldier/domain-list-custom/cn.txt](https://github.com/Loyalsoldier/domain-list-custom) 和 [blackmatrix7/ios_rule_script/ChinaMax](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)（仅域名）组合  
㉑ `rule-set,netflixip,🎥 奈飞视频` 源采用 [GeoLite2/netflix.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) 和 [blackmatrix7/ios_rule_script/Netflix](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)（仅 IP）组合  
㉒ `rule-set,telegramip,📲 电报消息` 源采用 [GeoLite2/telegram.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[Telegram IP 段](https://core.telegram.org/resources/cidr.txt) 和 [blackmatrix7/ios_rule_script/Telegram](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Telegram)（仅 IP）组合  
㉓ `rule-set,privateip,🔒 私有网络` 源采用 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（仅 IP）  
㉔ `rule-set,cnip,🇨🇳 国内 IP` 源采用 [GeoLite2/cn.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[17mon/china_ip_list](https://github.com/17mon/china_ip_list)、[gaoyifan/china-operator-ip](https://github.com/gaoyifan/china-operator-ip) 和 [blackmatrix7/ios_rule_script/ChinaIPs/ChinaIPs_IP.txt](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaIPs) 组合
## 3. 文件使用
### ① Clash 内核
- 注：以下只是节选，请酌情套用

```
proxy-groups:
  - {name: 📈 网络测试, type: select, proxies: [🎯 全球直连, 🇭🇰 香港节点, 🇹🇼 台湾节点, 🇯🇵 日本节点, 🇰🇷 韩国节点, 🇸🇬 新加坡节点, 🇺🇸 美国节点]}
  - {name: 🔗 直连域名, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}
  - {name: 🪜 代理域名, type: select, proxies: [🚀 节点选择, 🎯 全球直连]}
  - {name: 🎮 游戏平台, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}
  - {name: 🎥 奈飞视频, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 📽️ 迪士尼+, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 🎞️ Max, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 🎬 Prime Video, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 🍎 Apple TV+, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 📹 油管视频, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 🎵 TikTok, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 📺 哔哩哔哩, type: select, proxies: [🎯 全球直连, 🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 🤖 人工智能, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点, 🇺🇸 美国节点]}
  - {name: Ⓜ️ 微软服务, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}
  - {name: 📢 谷歌服务, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}
  - {name: 🍎 苹果服务, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}
  - {name: 🇨🇳 国内 IP, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}
  - {name: 📲 电报消息, type: select, proxies: [🚀 节点选择]}
  - {name: 🖥️ 直连软件, type: select, proxies: [🎯 全球直连]}
  - {name: 🔒 私有网络, type: select, proxies: [🎯 全球直连]}
  - {name: 🛑 广告拦截, type: select, proxies: [REJECT]}
  - {name: 🎯 全球直连, type: select, proxies: [DIRECT]}

rule-providers:
  ads:
    type: http
    behavior: domain
    format: text
    path: ./rules/ads.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/ads.list"
    interval: 86400

  applications:
    type: http
    behavior: classical
    format: text
    path: ./rules/applications.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/applications.list"
    interval: 86400

  private:
    type: http
    behavior: domain
    format: text
    path: ./rules/private.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/private.list"
    interval: 86400

  microsoft-cn:
    type: http
    behavior: domain
    format: text
    path: ./rules/microsoft-cn.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/microsoft-cn.list"
    interval: 86400

  apple-cn:
    type: http
    behavior: domain
    format: text
    path: ./rules/apple-cn.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/apple-cn.list"
    interval: 86400

  google-cn:
    type: http
    behavior: domain
    format: text
    path: ./rules/google-cn.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/google-cn.list"
    interval: 86400

  games-cn:
    type: http
    behavior: domain
    format: text
    path: ./rules/games-cn.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/games-cn.list"
    interval: 86400

  netflix:
    type: http
    behavior: domain
    format: text
    path: ./rules/netflix.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/netflix.list"
    interval: 86400

  disney:
    type: http
    behavior: domain
    format: text
    path: ./rules/disney.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/disney.list"
    interval: 86400

  max:
    type: http
    behavior: domain
    format: text
    path: ./rules/max.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/max.list"
    interval: 86400

  primevideo:
    type: http
    behavior: domain
    format: text
    path: ./rules/primevideo.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/primevideo.list"
    interval: 86400

  appletv:
    type: http
    behavior: domain
    format: text
    path: ./rules/appletv.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/appletv.list"
    interval: 86400

  youtube:
    type: http
    behavior: domain
    format: text
    path: ./rules/youtube.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/youtube.list"
    interval: 86400

  tiktok:
    type: http
    behavior: domain
    format: text
    path: ./rules/tiktok.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/tiktok.list"
    interval: 86400

  bilibili:
    type: http
    behavior: domain
    format: text
    path: ./rules/bilibili.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/bilibili.list"
    interval: 86400

  ai:
    type: http
    behavior: domain
    format: text
    path: ./rules/ai.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/ai.list"
    interval: 86400

  networktest:
    type: http
    behavior: classical
    format: text
    path: ./rules/networktest.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/networktest.list"
    interval: 86400

  proxy:
    type: http
    behavior: domain
    format: text
    path: ./rules/proxy.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/proxy.list"
    interval: 86400

  cn:
    type: http
    behavior: domain
    format: text
    path: ./rules/cn.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/cn.list"
    interval: 86400

  netflixip:
    type: http
    behavior: ipcidr
    format: text
    path: ./rules/netflixip.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/netflixip.list"
    interval: 86400

  telegramip:
    type: http
    behavior: ipcidr
    format: text
    path: ./rules/telegramip.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/telegramip.list"
    interval: 86400

  privateip:
    type: http
    behavior: ipcidr
    format: text
    path: ./rules/privateip.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/privateip.list"
    interval: 86400

  cnip:
    type: http
    behavior: ipcidr
    format: text
    path: ./rules/cnip.list
    url: "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-ruleset/cnip.list"
    interval: 86400

rules:
  - RULE-SET,ads,🛑 广告拦截
  - RULE-SET,applications,🖥️ 直连软件
  - RULE-SET,private,🔒 私有网络
  - RULE-SET,microsoft-cn,Ⓜ️ 微软服务
  - RULE-SET,apple-cn,🍎 苹果服务
  - RULE-SET,google-cn,📢 谷歌服务
  - RULE-SET,games-cn,🎮 游戏平台
  - RULE-SET,netflix,🎥 奈飞视频
  - RULE-SET,disney,📽️ 迪士尼+
  - RULE-SET,max,🎞️ Max
  - RULE-SET,primevideo,🎬 Prime Video
  - RULE-SET,appletv,🍎 Apple TV+
  - RULE-SET,youtube,📹 油管视频
  - RULE-SET,tiktok,🎵 TikTok
  - RULE-SET,bilibili,📺 哔哩哔哩
  - RULE-SET,ai,🤖 人工智能
  - RULE-SET,networktest,📈 网络测试
  - RULE-SET,proxy,🪜 代理域名
  - RULE-SET,cn,🔗 直连域名
  - RULE-SET,netflixip,🎥 奈飞视频
  - RULE-SET,telegramip,📲 电报消息
  - RULE-SET,privateip,🔒 私有网络,no-resolve
  - RULE-SET,cnip,🇨🇳 国内 IP
```
### ② sing-box 内核
- 注：以下只是节选，请酌情套用

```
{
  "outbounds": [
    { "tag": "🚀 节点选择", "type": "selector", "outbounds": [ "🇭🇰 香港节点", "🇹🇼 台湾节点", "🇯🇵 日本节点", "🇰🇷 韩国节点", "🇸🇬 新加坡节点", "🇺🇸 美国节点" ] },
    { "tag": "📈 网络测试", "type": "selector", "outbounds": [ "🎯 全球直连", "🇭🇰 香港节点", "🇹🇼 台湾节点", "🇯🇵 日本节点", "🇰🇷 韩国节点", "🇸🇬 新加坡节点", "🇺🇸 美国节点" ] },
    { "tag": "🔗 直连域名", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择" ] },
    { "tag": "🪜 代理域名", "type": "selector", "outbounds": [ "🚀 节点选择", "🎯 全球直连" ] },
    { "tag": "🎮 游戏平台", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择" ] },
    { "tag": "🎥 奈飞视频", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "📽️ 迪士尼+", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "🎞️ Max", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "🎬 Prime Video", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "🍎 Apple TV+", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "📹 油管视频", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "🎵 TikTok", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "📺 哔哩哔哩", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "🤖 人工智能", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点", "🇺🇸 美国节点" ] },
    { "tag": "Ⓜ️ 微软服务", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择" ] },
    { "tag": "📢 谷歌服务", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择" ] },
    { "tag": "🍎 苹果服务", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择" ] },
    { "tag": "🇨🇳 国内 IP", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择" ] },
    { "tag": "📲 电报消息", "type": "selector", "outbounds": ["🚀 节点选择"] },
    { "tag": "🖥️ 直连软件", "type": "selector", "outbounds": ["🎯 全球直连"] },
    { "tag": "🔒 私有网络", "type": "selector", "outbounds": ["🎯 全球直连"] },
    { "tag": "🛑 广告拦截", "type": "selector", "outbounds": ["REJECT"] },
    { "tag": "🎯 全球直连", "type": "selector", "outbounds": ["DIRECT"] },
    { "tag": "REJECT", "type": "block" },
    { "tag": "DIRECT", "type": "direct" }
  ],
  "route": {
    "rules": [
      { "rule_set": [ "ads" ], "outbound": "🛑 广告拦截" },
      { "rule_set": [ "applications" ], "outbound": "🖥️ 直连软件" },
      { "rule_set": [ "private" ], "outbound": "🔒 私有网络" },
      { "rule_set": [ "microsoft-cn" ], "outbound": "Ⓜ️ 微软服务" },
      { "rule_set": [ "apple-cn" ], "outbound": "🍎 苹果服务" },
      { "rule_set": [ "google-cn" ], "outbound": "📢 谷歌服务" },
      { "rule_set": [ "games-cn" ], "outbound": "🎮 游戏平台" },
      { "rule_set": [ "netflix" ], "outbound": "🎥 奈飞视频" },
      { "rule_set": [ "disney" ], "outbound": "📽️ 迪士尼+" },
      { "rule_set": [ "max" ], "outbound": "🎞️ Max" },
      { "rule_set": [ "primevideo" ], "outbound": "🎬 Prime Video" },
      { "rule_set": [ "appletv" ], "outbound": "🍎 Apple TV+" },
      { "rule_set": [ "youtube" ], "outbound": "📹 油管视频" },
      { "rule_set": [ "tiktok" ], "outbound": "🎵 TikTok" },
      { "rule_set": [ "bilibili" ], "outbound": "📺 哔哩哔哩" },
      { "rule_set": [ "ai" ], "outbound": "🤖 人工智能" },
      { "rule_set": [ "networktest" ], "outbound": "📈 网络测试" },
      { "rule_set": [ "proxy" ], "outbound": "🪜 代理域名" },
      { "rule_set": [ "cn" ], "outbound": "🔗 直连域名" },
      { "rule_set": [ "netflixip" ], "outbound": "🎥 奈飞视频" },
      { "rule_set": [ "telegramip" ], "outbound": "📲 电报消息" },
      { "rule_set": [ "privateip" ], "outbound": "🔒 私有网络" },
      { "rule_set": [ "cnip" ], "outbound": "🇨🇳 国内 IP" }
    ],
    "rule_set": [
      {
        "tag": "ads",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/ads.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "applications",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/applications.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "private",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/private.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "microsoft-cn",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/microsoft-cn.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "apple-cn",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/apple-cn.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "google-cn",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/google-cn.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "games-cn",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/games-cn.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "netflix",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/netflix.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "disney",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/disney.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "max",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/max.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "primevideo",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/primevideo.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "appletv",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/appletv.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "youtube",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/youtube.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "tiktok",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/tiktok.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "bilibili",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/bilibili.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "ai",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/ai.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "networktest",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/networktest.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "proxy",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/proxy.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "cn",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/cn.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "netflixip",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/netflixip.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "telegramip",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/telegramip.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "privateip",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/privateip.srs",
        "download_detour": "DIRECT"
      },
      {
        "tag": "cnip",
        "type": "remote",
        "format": "binary",
        "url": "https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-ruleset/cnip.srs",
        "download_detour": "DIRECT"
      }
    ]
  }
}
```
## 4. 文件拓展
### ① [user.yaml](https://github.com/DustinWin/ruleset_geodata/tree/clash-config)（仅限 mihomo 内核）
- 注：含有“fakeip”字样的 .yaml 配置文件中才含有 `fake-ip-filter` 参数

**配置文件名关键字与使用场景对应关系如下表：**
|文件名关键字|使用场景|
|-----|-----|
|lite|无广告拦截，搭配 AdGuardHome|
|noprocess|不含进程匹配模式，仅适合 ShellCrash|

• `fake-ip-filter` 参数  
`fake-ip-filter` 中添加[常用 fake-ip 地址过滤列表](https://github.com/juewuy/ShellCrash/blob/master/public/fake_ip_filter.list)，提高兼容性  
`fake-ip-filter` 中添加 [TrackersList](https://github.com/XIU2/TrackersListCollection/blob/master/all.txt)（udp 域名），防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition)无法连接 TrackersList UDP 协议  
<img src="https://user-images.githubusercontent.com/45238096/224113233-4d76dec2-495c-4790-a00e-538fc1469639.png" width="60%"/>  
`fake-ip-filter` 中添加 AdGuardHome 相关域名，包括：`adguardteam.github.io`（AdGuardHome 自带 DNS 黑名单下载域名）、`adrules.top`（常用广告拦截下载域名）、`anti-ad.net`（常用广告拦截下载域名）和 `static.adtidy.org`（AdGuardHome 检查更新域名），防止作为下游时检查更新和下载“DNS 黑名单”失败  
若想自己生成配置文件 user.yaml，可以 [Fork 本项目](https://github.com/DustinWin/ruleset_geodata/fork)后编辑 *.github/workflows/build.yml* 文件内的 ```name: Generate `clash` ruleset-xxx-user.yaml``` 部分  
若 DNS 模式选用的是 `redir-host`，必须进行 DNS 分流（可以参考 [mihomo 内核 DNS 分流教程](https://github.com/DustinWin/clash_singbox-tutorials/tree/main/%E6%95%99%E7%A8%8B%E5%90%88%E9%9B%86/Clash/%E8%BF%9B%E9%98%B6%E7%AF%87)），可以进入 *.github/workflows/build.yml* 文件，编辑 ```Generate `clash` ruleset-redirhost-user.yaml``` 部分，将 `nameserver` 中的 `🪜 代理域名` 改成可以访问外网的策略组名称，或者直接将 `'https://dns.google/dns-query#🪜 代理域名'` 修改为 `'tls://dns.google'`  
• 导入 Linux 端（以导入 ShellCrash 为例）  
将下面命令中的 `{DNS 模式}` 替换为正在使用的 DNS 模式（`fakeip` 或 `redirhost`）  
连接 SSH 后执行如下命令：
```
curl -o $CRASHDIR/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-config/ruleset-{DNS 模式}-user-lite-noprocess.yaml
$CRASHDIR/start.sh restart
```
• 导入 Windows 端（以导入 Clash Verge 为例）  
首次使用可进入 Clash Verge->订阅，新建“Merge”类型的配置，完成后点击“保存”，右击新建的 Merge 文件，点击“启用”  
进入文件夹 *%APPDATA%\io.github.clash-verge-rev.clash-verge-rev\profiles*，找到与上一步新建的 Merge 文件相对应的 .yaml 文件，复制其文件名并替换下面命令中的 `{Merge 文件名}`
将下面命令中的 `{DNS 模式}` 替换为正在使用的 DNS 模式（`fakeip` 或 `redirhost`）  
以管理员身份打开 CMD 命令提示符，执行如下命令：
```
taskkill /f /t /im "Clash Verge*"
taskkill /f /t /im Clash-Verge*
taskkill /f /t /im clash-meta*
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\profiles\{Merge 文件名}.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-config/ruleset-{DNS 模式}-user.yaml
```
### ② [dns.json](https://github.com/DustinWin/ruleset_geodata/tree/sing-box-config)（仅限 sing-box PuerNya 版内核）
- 注：含有“lite”后缀的 .json 配置文件适合无 sing-box 广告拦截且配合 [AdGuardHome](https://github.com/AdguardTeam/AdGuardHome) 的方案

• `dns.rules` 数组  
`dns.rules` 中添加 AdGuardHome 相关域名，包括：`adguardteam.github.io`（AdGuardHome 自带 DNS 黑名单下载域名）、`adrules.top`（常用广告拦截下载域名）、`anti-ad.net`（常用广告拦截下载域名）和 `static.adtidy.org`（AdGuardHome 检查更新域名），防止作为下游时检查更新和下载“DNS 黑名单”失败  
• 导入 Linux 端（以导入 ShellCrash 为例）   
连接 SSH 后执行如下命令：
```
curl -o $CRASHDIR/jsons/dns.json -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-config/ruleset-dns-lite.json
$CRASHDIR/start.sh restart
```
### ③ 添加定时任务（以 ShellCrash 为例，安装路径为 */data/ShellCrash*）
• 连接 SSH 后执行 `vi $CRASHDIR/task/task.user`，按一下 Ins 键（Insert 键），粘贴如下内容：
```
# 适用于 mihomo 内核
201#curl -o /data/ShellCrash/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-config/ruleset-{DNS 模式}-user-lite-noprocess.yaml && /data/ShellCrash/start.sh restart >/dev/null 2>&1#更新user.yaml
```
• 按一下 Esc 键（退出键），输入英文冒号 `:`，继续输入 `wq` 并回车  
• 执行 `crash`，进入 ShellCrash->5 配置自动任务->1 添加自动任务，可以看到末尾就有添加的定时任务，输入对应的数字并回车后可设置执行条件

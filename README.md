# 一、 说明
## 1. geosite.dat
① 在 [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat) 的基础上进行修改，请酌情使用，**仅有如下分类**：  
```
geosite:category-ads-all # ⛔️ 广告域名
geosite:private # 🏠 私有网络
geosite:tracker # ⛓️ BT 下载
geosite:network # 📈 网络测试
geosite:microsoft-cn # Ⓜ️ Microsoft 中国
geosite:apple-cn # 🍎 Apple 中国
geosite:google-cn # 🗽 Google 中国
geosite:games-cn # 🎮 国区游戏
geosite:geolocation-!cn # 🪜 国外域名
geosite:cn # 🇨🇳 国内域名
```
② 每天早上 3 点（北京时间）自动构建  
③ 将 `geosite:category-ads-all` 源修改为 [blackmatrix7/ios_rule_script/Advertising](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Advertising)  
④ 新增分类 `geosite:tracker`，源采用 [blackmatrix7/ios_rule_script/PrivateTracker](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/PrivateTracker)  
⑤ 新增分类 `geosite:network`，源采用 [blackmatrix7/ios_rule_script/Speedtest](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Speedtest)、[v2fly/domain-list-community/data/test-ipv6](https://github.com/v2fly/domain-list-community/blob/master/data/test-ipv6) 和 [IPv6 测试网站](https://github.com/DustinWin/clash-geosite/blob/master/Rule-Files/network.txt)组合  
⑥ 新增分类 `geosite:microsoft-cn`，源采用 [v2fly/domain-list-community/data/microsoft](https://github.com/v2fly/domain-list-community/blob/master/data/microsoft)（包含“include”且含有“@cn”的所有域名）  
⑦ 新增分类 `geosite:games-cn`，源采用 [blackmatrix7/ios_rule_script/SteamCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/SteamCN) 和 [blackmatrix7/ios_rule_script/GameDownloadCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Game/GameDownloadCN) 组合  
⑧ 将 `geosite:geolocation-!cn` 源修改为 [blackmatrix7/ios_rule_script/Proxy](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Proxy)，并新增 `DOMAIN-SUFFIX,googleapis.cn`，防止出现 [Google Play Store](https://play.google.com/store) 无法下载或升级应用的问题  
⑨ 将 `geosite:cn` 源修改为 [blackmatrix7/ios_rule_script/ChinaMax](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)  
⑩ 删除“Windows 操作系统相关的系统升级和隐私跟踪域名”，包括 `geosite:win-spy`、`geosite:win-update` 和 `geosite:win-extra`
## 2. geoip.dat 和 Country.mmdb
① 在 [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip) 的基础上进行修改  
② 只保留 `geoip:cn`、`geoip:private` 和 `geoip:telegram` 部分，刚好对应我所建 [Clash 规则模板](https://github.com/DustinWin/Router-Plugins/tree/main/Rule-Templates)中 rules 里的 3 项
# 二、 下载
## 1. geosite.dat
① GitHub 源：https://github.com/DustinWin/clash-geosite/releases/download/latest/geosite.dat  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite.dat
## 2. geoip.dat
① GitHub 源：https://github.com/DustinWin/clash-geoip/releases/download/latest/geoip.dat  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geoip@release/geoip.dat
## 3. Country.mmdb
① GitHub 源：https://github.com/DustinWin/clash-geoip/releases/download/latest/Country.mmdb  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geoip@release/Country.mmdb
# 三、 导入
## 1. 导入 ShellClash
```
curl -o $clashdir/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite.dat
curl -o $clashdir/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geoip@release/geoip.dat
curl -o $clashdir/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geoip@release/Country.mmdb
```
## 2. 导入 Clash Verge（Windows 端）
```
curl -o %USERPROFILE%\.config\clash-verge\geosite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite.dat
curl -o %USERPROFILE%\.config\clash-verge\geoip.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geoip@release/geoip.dat
curl -o %USERPROFILE%\.config\clash-verge\Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geoip@release/Country.mmdb
copy /y "%USERPROFILE%\.config\clash-verge\geosite.dat" "%PROGRAMFILES%\Clash Verge\resources"
copy /y "%USERPROFILE%\.config\clash-verge\geoip.dat" "%PROGRAMFILES%\Clash Verge\resources"
copy /y "%USERPROFILE%\.config\clash-verge\Country.mmdb" "%PROGRAMFILES%\Clash Verge\resources"
```

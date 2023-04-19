# 一、 说明
## 1. geosite.dat
① 根据 [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat) 进行深度定制，**有且仅有如下分类**：
```
- GEOSITE,advertising,⛔️ 广告域名
- GEOSITE,lan,🏠 私有网络
- GEOSITE,tracker,⛓️ BT 下载
- GEOSITE,networktest,📈 网络测试
- GEOSITE,microsoft-cn,Ⓜ️ Microsoft 中国
- GEOSITE,apple-cn,🍎 Apple 中国
- GEOSITE,google-cn,🗽 Google 中国
- GEOSITE,games-cn,🎮 国区游戏
- GEOSITE,proxy,🪜 代理域名
- GEOSITE,cn,🚄 直连域名
```
② 每天早上 3 点（北京时间）自动构建    
③ `geosite:advertising` 源采用 [blackmatrix7/ios_rule_script/Advertising](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Advertising)  
④ `geosite:lan` 源采用 [blackmatrix7/ios_rule_script/Lab](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)  
⑤ `geosite:tracker` 源采用 [blackmatrix7/ios_rule_script/PrivateTracker](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/PrivateTracker)  
⑥ `geosite:networktest` 源采用 [blackmatrix7/ios_rule_script/Speedtest](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Speedtest) 和 [IPv6 测试网站](https://github.com/DustinWin/clash-geosite/blob/master/Rule-Files/network.txt)组合   
⑦ `geosite:microsoft-cn` 源采用 [rules.kr328.app/microsoft@cn](https://rules.kr328.app/microsoft@cn.yaml)、[rules.kr328.app/microsoft-dev@cn](https://rules.kr328.app/microsoft-dev@cn.yaml) 和 [rules.kr328.app/microsoft-pki@cn](https://rules.kr328.app/microsoft-pki@cn.yaml) 组合  
⑧ `geosite:apple-cn` 源采用 [rules.kr328.app/apple@cn](https://rules.kr328.app/apple@cn.yaml)、[rules.kr328.app/apple-dev@cn](https://rules.kr328.app/apple-dev@cn.yaml) 和 [rules.kr328.app/apple-pki@cn](https://rules.kr328.app/apple-pki@cn.yaml) 组合  
⑨ `geosite:google-cn` 源采用 [rules.kr328.app/google@cn](https://rules.kr328.app/google@cn.yaml)（删除 googleapis.cn，以免直连时出现 [Google Play Store](https://play.google.com/store) 无法下载或升级应用的问题）和 [rules.kr328.app/google-trust-services@cn](https://rules.kr328.app/google-trust-services@cn.yaml) 组合  
⑩ `geosite:games-cn` 源采用 [rules.kr328.app/category-games@cn](https://rules.kr328.app/category-games@cn.yaml)  
⑪ `geosite:proxy` 源采用 [blackmatrix7/ios_rule_script/Proxy](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Proxy)，并新增 `DOMAIN-SUFFIX,googleapis.cn`，防止出现 Google Play Store 无法下载或升级应用的问题  
⑫ `geosite:cn` 源采用 [blackmatrix7/ios_rule_script/ChinaMax](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)
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

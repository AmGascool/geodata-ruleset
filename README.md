# 一、 说明
## 1. geosite.dat
① 根据 [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat) 进行深度定制，**有且仅有如下分类**：
```
- GEOSITE,advertising,⛔️ 广告域名
- GEOSITE,lan,🏠 私有网络
- GEOSITE,networktest,📈 网络测试
- GEOSITE,microsoft-cn,Ⓜ️ Microsoft 中国
- GEOSITE,apple-cn,🍎 Apple 中国
- GEOSITE,google-cn,🗽 Google 中国
- GEOSITE,games-cn,🎮 国区游戏
- GEOSITE,proxy,🪜 代理域名
- GEOSITE,cn,🇨🇳 国内域名
```
② 每天早上 3 点（北京时间）自动构建  
③ `geosite:advertising` 源采用 [blackmatrix7/ios_rule_script/Advertising](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Advertising)  
④ `geosite:lan` 源采用 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)  
⑤ `geosite:networktest` 源采用 [blackmatrix7/ios_rule_script/Speedtest](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Speedtest) 和 [IPv6 测试网站](https://github.com/DustinWin/clash-geosite/blob/master/rule-files/network.txt)组合   
⑥ `geosite:microsoft-cn` 源采用 [rules.kr328.app/microsoft@cn](https://rules.kr328.app/microsoft@cn.yaml)  
⑦ `geosite:apple-cn` 源采用 [rules.kr328.app/apple@cn](https://rules.kr328.app/apple@cn.yaml)  
⑧ `geosite:google-cn` 源采用 [rules.kr328.app/google@cn](https://rules.kr328.app/google@cn.yaml)（删除 `DOMAIN-SUFFIX,googleapis.cn`，以免直连时出现 [Google Play Store](https://play.google.com/store) 无法下载或升级应用的问题）  
⑨ `geosite:games-cn` 源采用 [rules.kr328.app/category-games@cn](https://rules.kr328.app/category-games@cn.yaml)  
⑩ `geosite:proxy` 源采用 [blackmatrix7/ios_rule_script/Proxy](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Proxy)  
⑪ `geosite:cn` 源采用 [blackmatrix7/ios_rule_script/ChinaMax](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)
## 2. geoip.dat 和 Country.mmdb
① 在 [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip) 的基础上进行修改  
② 每天早上 3 点（北京时间）自动构建  
③ 只保留 `geoip:cn`、`geoip:private` 和 `geoip:telegram` 部分，刚好对应我所建 [Clash 规则模板](https://github.com/DustinWin/clash-tutorials/blob/main/rule-templates/geo-mode/template_whitelist.yaml)中 rules 里的 3 项
## 3. user.yaml
① 每天早上 3 点（北京时间）自动构建生成  
② 若想自己生成配置文件 user.yaml，可以 [Fork 本项目](https://github.com/DustinWin/clash-geosite/fork)后编辑 *.github/workflows/run.yml* 内的 `name: Put together user.yaml` 部分和 *User-Config* 目录下的.yaml 文件  
③ 编辑 *User-Config/later-user.yaml* 文件，将 `nameserver` 中的`🪜 代理域名`改成可以访问外网的代理组名，或者直接将 `'https://dns.google/dns-query#🪜 代理域名'`修改为 `tls://dns.google`  
④ 添加 [NTP 服务](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/NTPService)到 user.yaml 内的 `fake-ip-filter` 中，防止校时失败  
⑤ 添加 [TrackersList](https://trackerslist.com) 到 user.yaml 内的 `fake-ip-filter` 中，防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition)无法连接 TrackersList UDP 协议
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
连接 SSH 后执行如下命令：
```
curl -o $clashdir/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite.dat
curl -o $clashdir/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geoip@release/geoip.dat
curl -o $clashdir/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geoip@release/Country.mmdb
curl -o $clashdir/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/user.yaml
```
## 2. 导入 Clash Verge（Windows 端）
首次使用可进入“配置”，新建”Merge“类型的配置，保存后进入文件夹 *%USERPROFILE%\.config\clash-verge\profiles*，可以看到这里新增了一个.yaml 文件，复制其文件名并替换下面命令中的{文件名}  
编辑文本文档，粘贴如下内容：
```
curl -o %USERPROFILE%\.config\clash-verge\geosite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite.dat
curl -o %USERPROFILE%\.config\clash-verge\geoip.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geoip@release/geoip.dat
curl -o %USERPROFILE%\.config\clash-verge\Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geoip@release/Country.mmdb
copy /y "%USERPROFILE%\.config\clash-verge\geosite.dat" "%PROGRAMFILES%\Clash Verge\resources"
copy /y "%USERPROFILE%\.config\clash-verge\geoip.dat" "%PROGRAMFILES%\Clash Verge\resources"
copy /y "%USERPROFILE%\.config\clash-verge\Country.mmdb" "%PROGRAMFILES%\Clash Verge\resources"
curl -o %USERPROFILE%\.config\clash-verge\profiles\{文件名}.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/user.yaml
```
另存为.bat 文件，右击该文件，选择以管理员身份运行

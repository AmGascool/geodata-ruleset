# 一、 说明
## 1. geosite.dat
① 根据 [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat) 进行深度定制，**有且仅有如下分类**：
```
  - GEOSITE,ads,⛔️ 广告域名
  - GEOSITE,lan,🏠 私有网络
  - GEOSITE,networktest,📈 网络测试
  - GEOSITE,microsoft-cn,Ⓜ️ Microsoft 中国
  - GEOSITE,apple-cn,🍎 Apple 中国
  - GEOSITE,google-cn,🗽 Google 中国
  - GEOSITE,games-cn,🎮 国区游戏
  - GEOSITE,proxy,🪜 代理域名
  - GEOSITE,cn,⚡ 直连域名
```
② 每天早上 3 点（北京时间）自动构建  
③ `geosite:ads` 源采用 [privacy-protection-tools/anti-AD](https://github.com/privacy-protection-tools/anti-AD)  
④ `geosite:lan` 源采用 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（域名部分）  
⑤ `geosite:networktest` 源采用 [blackmatrix7/ios_rule_script/Speedtest](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Speedtest) 和 [IPv6 测试网站](https://github.com/DustinWin/clash-geosite/blob/master/rule-files/network.txt)组合   
⑥ `geosite:microsoft-cn` 源采用 [rules.kr328.app/microsoft@cn](https://rules.kr328.app/microsoft@cn.yaml)  
⑦ `geosite:apple-cn` 源采用 [rules.kr328.app/apple@cn](https://rules.kr328.app/apple@cn.yaml)  
⑧ `geosite:google-cn` 源采用 [rules.kr328.app/google@cn](https://rules.kr328.app/google@cn.yaml)（删除 `DOMAIN-SUFFIX,googleapis.cn`，以免直连时出现 [Google Play Store](https://play.google.com/store) 无法下载或升级应用的问题）  
⑨ `geosite:games-cn` 源采用 [rules.kr328.app/category-games@cn](https://rules.kr328.app/category-games@cn.yaml)  
⑩ `geosite:proxy` 源采用 [Loyalsoldier/domain-list-custom](://github.com/Loyalsoldier/domain-list-custom)  
⑪ `geosite:cn` 源采用 [blackmatrix7/ios_rule_script/ChinaMax](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)
## 2. geosite-lite.dat
在 geosite.dat 的基础上去除了广告域名 `geosite:ads`，**有且仅有如下分类**：
```
  - GEOSITE,lan,🏠 私有网络
  - GEOSITE,networktest,📈 网络测试
  - GEOSITE,microsoft-cn,Ⓜ️ Microsoft 中国
  - GEOSITE,apple-cn,🍎 Apple 中国
  - GEOSITE,google-cn,🗽 Google 中国
  - GEOSITE,games-cn,🎮 国区游戏
  - GEOSITE,proxy,🪜 代理域名
  - GEOSITE,cn,⚡ 直连域名
```
## 3. geoip.dat 和 Country.mmdb
① 数据来源 [DustinWin/clash-geoip](https://github.com/DustinWin/clash-geoip)，**有且仅有如下分类**：
```
  - GEOIP,cn,🇨🇳 国内 IP
  - GEOIP,lanip,🏠 私有网络
  - GEOIP,telegramip,✈️ Telegram IP
```
② 每天早上 3 点（北京时间）自动构建  
③ `geoip:cn` 源采用 [blackmatrix7/ios_rule_script/ChinaMax](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)（ChinaMax_IP.txt）、[17mon/china_ip_list](https://github.com/17mon/china_ip_list) 和 [gaoyifan/china-operator-ip](https://github.com/gaoyifan/china-operator-ip) 组合  
④ `geoip:lanip` 源采用 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（IP 部分）  
⑤ `geoip:telegramip` 源采用 [Telegram IP](https://core.telegram.org/resources/cidr.txt)
## 4. user.yaml
① 每天早上 3 点（北京时间）自动构建生成  
② 添加[常用 fake-ip 地址过滤列表](https://github.com/juewuy/ShellClash/blob/master/public/fake_ip_filter.list)到 fake-ip-user.yaml 内的 `fake-ip-filter` 中，提高兼容性  
③ 添加 [TrackersList](https://trackerslist.com) 到 fake-ip-user.yaml 内的 `fake-ip-filter` 中，防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition/releases)无法连接 TrackersList UDP 协议  
<img src="https://user-images.githubusercontent.com/45238096/224113233-4d76dec2-495c-4790-a00e-538fc1469639.png" width="60%"/>  

④ 添加如下域名，以配合 AdGuardHome 作为下游来下载黑名单：
```
    - adguardteam.github.io
    - anti-ad.net
```
⑤ 若想自己生成配置文件 user.yaml，可以 [Fork 本项目](https://github.com/DustinWin/clash-geosite/fork)后编辑 *.github/workflows/run.yml* 文件内的 `name: Generate xxx-user.yaml` 部分  
⑥ 若 DNS 模式选用的是 redir-host，需要进行 [DNS 分流](https://github.com/DustinWin/clash-tutorials/blob/main/%E6%95%99%E7%A8%8B%E5%90%88%E9%9B%86/%E8%BF%9B%E9%98%B6%E7%AF%87/ShellClash%20%E4%BD%BF%E7%94%A8%20Clash.Meta%20%E5%86%85%E6%A0%B8%E8%BF%9B%E8%A1%8C%20DNS%20%E5%88%86%E6%B5%81%E6%95%99%E7%A8%8B%20geo%20%E6%96%B9%E6%A1%88.md)，可以进入 *.github/workflows/run.yml* 文件，编辑 `Generate redir-host-user.yaml` 部分，将 `nameserver` 中的 `🪜 代理域名`改成可以访问外网的代理组名，或者直接将 `'https://dns.google/dns-query#🪜 代理域名'` 修改为 `'tls://dns.google'`
# 二、 下载
## 1. geosite.dat
① GitHub 源：https://github.com/DustinWin/clash-geosite/releases/download/latest/geosite.dat  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite.dat
## 2. geosite-lite.dat
① GitHub 源：https://github.com/DustinWin/clash-geosite/releases/download/latest/geosite-lite.dat  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite-lite.dat
## 3. geoip.dat
① GitHub 源：https://github.com/DustinWin/clash-geosite/releases/download/latest/geoip.dat  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geoip.dat
## 4. Country.mmdb
① GitHub 源：https://github.com/DustinWin/clash-geosite/releases/download/latest/Country.mmdb  
② jsDelivr 源：https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/Country.mmdb
# 三、 导入 [ShellClash](https://github.com/juewuy/ShellClash)
## 1. DNS 模式为 fake-ip  
连接 SSH 后执行如下命令：
- 注：以 geosite.dat 为例

```
curl -o $clashdir/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite.dat
curl -o $clashdir/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geoip.dat
curl -o $clashdir/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/Country.mmdb
curl -o $clashdir/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/fake-ip-user.yaml
$clashdir/start.sh restart
```
## 2. DNS 模式为 redir-host  
连接 SSH 后执行如下命令：
- 注：以 geosite.dat 为例

```
curl -o $clashdir/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geosite.dat
curl -o $clashdir/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/geoip.dat
curl -o $clashdir/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/Country.mmdb
curl -o $clashdir/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/clash-geosite@release/redir-host-user.yaml
$clashdir/start.sh restart
```

# 滲透測試
```
滲透測試是類比駭客的手法對網路或主機進行攻擊測試，為的是發掘系統漏洞、並提出改善方法
```
# ifconfig
```
用於組態、控制及查詢TCP/IP網路介面的系統管理工具
```
```
# ifconfig 查看IP
```
# netdiscover (ARP偵查工具)
```
# netdiscover -h 查看參數指令

常用指令參數：netdiscover [-P 埠口掃描(Port->服務掃描)][-O 作業系統掃描] [-sP Ping掃描(ping scan)]
[-i設備] [-r範圍| -l文件| -p] [-s時間] [-n節點] [-c計數] [-f] [-d] [-S] [-C]

# netdiscover -O 10.0.2.4 掃描目標IP可能的作業系統
Running:Microsoft Windows XP｜2003 目標IP作業系統可能是XP｜2003
# netdiscover -r 10.0.2.4 掃描目標IP範圍?
```
### ARP 位址解析協定 (Address Resolution Protocol,ARP)
```
在乙太網路協定中規定，同一區域網路中的一台主機要和另一台主機進行直接通信，必須要知道目標主機的MAC位址
```
### MAC位址
```
區域網路位址（LAN Address），乙太網路位址（Ethernet Address）或實體位址（Physical Address）
它是一個用來確認網路裝置位置的位址。在OSI模型中，第三層網路層負責IP位址，第二層資料鏈結層則負責MAC位址
```

# Nmap漏洞掃描
```
# namp -O 10.0.2.4 掃描目標IP漏洞
# namp --script vuln 10.0.2.4 掃描目標是否有常見的漏洞 (如MS-08-067)
```
### CVE 公共漏洞和暴露（Common Vulnerabilities and Exposures,CVE）
```
又稱常見漏洞與披露，是一個與資訊安全有關的資料庫，收集各種資安弱點及漏洞並給予編號以便於公眾查閱
```
### CVE-2020-0796 RCE漏洞

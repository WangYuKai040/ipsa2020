o# 滲透測試
```
滲透測試是類比駭客的手法對網路或主機進行攻擊測試，為的是發掘系統漏洞、並提出改善方法
```
# 查IP
```
ifconfig (linux)
ipconfig 查IP(Windows)
```
# netdiscover (ARP偵查工具)
```
# netdiscover -h 查看參數

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

# Nmap 漏洞掃描
https://blog.gtwang.org/linux/nmap-command-examples-tutorials/  
https://www.lijyyh.com/2012/03/nmap-using-nmap-security-scanner.html
```
Nmap兩大技術 1.一般掃描 2.nmap s
```
```
# namp -O 10.0.2.4 掃描目標IP漏洞
# namp --script vuln 10.0.2.4 掃描目標是否有常見的漏洞 (如MS-08-067)
```
### CVE 公共漏洞和暴露（Common Vulnerabilities and Exposures,CVE）
```
又稱常見漏洞與披露，是一個與資訊安全有關的資料庫，收集各種資安弱點及漏洞並給予編號以便於公眾查閱
```
### CVE-2020-0796 RCE漏洞
```
Windows 10和Windows Server操作系統存在這個漏洞
根據微軟的說法，攻擊者可以利用此漏洞在SMB服務器或SMB客戶端上執行任意代碼。攻擊者只要發送精心構造的數據包就能攻擊服務器。
而要想攻擊客戶端，攻擊者則須先配置一個惡意的SMBv3服務器，並讓用戶連接到它。
網路安全專家認為，該漏洞可被用於啟動類似WannaCry的蠕蟲病毒。微軟表示該漏洞非常嚴重，必須盡快關閉。
```
### 用戶該怎麼做？
```
SMB服務器：
通過PowerShell 指令阻止該漏洞被利用：
Set-ItemProperty -Path “HKLM:\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters” DisableCompression -Type DWORD -Value 1 –Force
SMB客戶端：
與應對WannaCry的方法一樣，微軟建議企業邊界防火牆關閉TCP端口445。
```
# netstat
http://aries.dyu.edu.tw/~tarng/dyu_c.c/netstat.htm
```
顯示通訊協定統計資料以及目前的 TCP/IP 網路連線
```
```
# netstat -h 查看參數
```
# taskkill 
```
此工具可依據處理程序識別碼(PID)或影像名稱來中止工作
```
```
taskkill/? 查看參數
taskkill /F 指定要強制終止的處理程序
```

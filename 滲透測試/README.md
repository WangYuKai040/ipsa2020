# 滲透測試
```
滲透測試是類比駭客的手法對網路或主機進行攻擊測試，為的是發掘系統漏洞、並提出改善方法
```
```
# ifconfig 查看linux IP
```
# netdiscover (ARP偵查工具)
```
# netdiscover -h 查看參數指令
用法：netdiscover [-i設備] [-r範圍| -l文件| -p] [-s時間] [-n節點] [-c計數] [-f] [-d] [-S] [-P] [-C]
# netdiscover -r 10.0.2.4 掃描指定IP範圍 
```
# Nmap漏洞掃描
```
# namp -o 10.0.2.4 (後面是目標IP)
# namp --script vuln 10.0.2.4 檢查目標是否有常見的漏洞 (如MS-08-067)

https://kknews.cc/zh-tw/code/xjaljar.html
```
# MAC位址
```
區域網路位址（LAN Address），乙太網路位址（Ethernet Address）或實體位址（Physical Address）
它是一個用來確認網路裝置位置的位址。在OSI模型中，第三層網路層負責IP位址，第二層資料鏈結層則負責MAC位址
```

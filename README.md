## 介绍
个人自用Clash规则，在ACL4SSR规则的基础上，添加了OpenAI，虚拟钱包等规则，之后也会持续更新

## 使用方式
如果使用的是SubConvertor工具，修改config字段为`https%3A//raw.githubusercontent.com/monlor/openclash-rules/master/ACL4SSR_Online_Full.ini`

## clash规则

* DOMAIN-SUFFIX：域名后缀匹配
* DOMAIN：域名匹配
* DOMAIN-KEYWORD：域名关键字匹配
* IP-CIDR：IP 段匹配
* SRC-IP-CIDR：源 IP 段匹配
* GEOIP：GEOIP 数据库（国家代码）匹配
* DST-PORT：目标端口匹配
* SRC-PORT：源端口匹配
* PROCESS-NAME：源进程名匹配
* RULE-SET：Rule Provider 规则匹配
* MATCH：全匹配

```
##- SCRIPT,quic,REJECT #shortcuts rule
##- SCRIPT,time-limit,REJECT #shortcuts rule

##- PROCESS-NAME,curl,DIRECT #匹配路由自身进程(curl直连)
##- DOMAIN-SUFFIX,google.com,Proxy #匹配域名后缀(交由Proxy代理服务器组)
##- DOMAIN-KEYWORD,google,Proxy #匹配域名关键字(交由Proxy代理服务器组)
##- DOMAIN,google.com,Proxy #匹配域名(交由Proxy代理服务器组)
##- DOMAIN-SUFFIX,ad.com,REJECT #匹配域名后缀(拒绝)
##- IP-CIDR,127.0.0.0/8,DIRECT #匹配数据目标IP(直连)
##- SRC-IP-CIDR,192.168.1.201/32,DIRECT #匹配数据发起IP(直连)
##- DST-PORT,80,DIRECT #匹配数据目标端口(直连)
##- SRC-PORT,7777,DIRECT #匹配数据源端口(直连)

##排序在上的规则优先生效,如添加（去除规则前的#号）：
##IP段：192.168.1.2-192.168.1.200 直连
##- SRC-IP-CIDR,192.168.1.2/31,DIRECT
##- SRC-IP-CIDR,192.168.1.4/30,DIRECT
```
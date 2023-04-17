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

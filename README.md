# ENS
dns over the eosio


# ENS
dns on the eosio

## 合约端协议类型
```
eosio://[type(options)].[contract-name]
```

| type     |意义      |开发状态 |
| ---- | ---- | ---- |
| dapp    | 直接获取 dapp 地址     | todo     |
| roadmap | 获取 roadmap     |  todo    |
| mail    | 获取邮件联系地址     |  todo    |


## 客户端协议类型
```
eosio://[contract-name]
eosio://dapp.[contract-name]
eosio://mail.[contract-name]
eosio://roadmap.[contract-name]
```


## 具体举例

用户输入
`eosio://eosbet`
客户端（通常为 dapp 浏览器）向符合 ENS 解析规则的合约调用服务，结果如下：
```
{
    "dapp":"https://dice.eosbet.io/",
    "roadmap":"https://www.eosbet.io/#roadmap",
    "mail":"mailto:ico@eosbet.io"
}
```

用户输入
`eosio://dapp.eosbet`
客户端（通常为 dapp 浏览器）向符合 ENS 解析规则的合约调用服务，结果如下：
```
https://dice.eosbet.io/
```

用户输入为
`eosio://roadmap.eosbet`
返回
```
"https://dice.eosbet.io/#"
```



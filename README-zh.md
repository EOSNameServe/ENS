## ENS -- EOSAccountNameService

一个基于 EOSIO 的 DNS 雏形。目前你可以通过合约绑定你的 url 或者 ip 地址，然后通过 rpc 或者任何可以连接到 EOSIO 的方式，查询到绑定的 url 或者 ip 地址。
举个栗子，你可以把 `enserve.bank` （一个 EOS 主网的账号）和 http://eosnameserve.github.io [绑定](http://eosnameserve.github.io)，然后你在 [chrome 插件](https://github.com/fengqiyue/ensProtocolParser)中输入你的账号就可以访问你绑定的网站地址

## 合约地址
[enserve.bank](https://bloks.io/account/enserve.bank)


## 使用方式

### 绑定 
你只需要 push action `binddapp` 到 `enserve.bank`就可以，这个 action 也支持更新操作。
实时上，你也可以绑定 ip 地址，这样你就不需要找域名商去域名解析了。

#### 用前端页面绑定
你需要一个 EOS 账号和 scatter 插件
网站地址:[ensnameserve](https://eosnameserve.github.io/#/)

#### 用 cleos 绑定
```
cleos push action enserve.bank binddapp '["https://eosnameserve.github.io","enserve.bank"]'  -p enserve.bank@active

```

#### 用 eosjs 绑定
// todo


### 查询

#### 用 chrome 插件直接访问
输入账号，会自动跳转到绑定的网站地址。插件具体内容：[chrome_plugin](https://github.com/fengqiyue/ensProtocolParser)

#### 用 cleos  查询

```
cleos get table enserve.bank [YOUR_CONTRACT_NAME] enstables
```

栗子: 查询 `enserve.bank` 信息。
```
•100% ➜ cleos_remote get table enserve.bank enserve.bank enstables
{
  "rows": [{
      "contract_name": "6120580929069623040",
      "dapp": "https://eosnameserve.github.io/"
    }
  ],
  "more": false
}
```
#### 用 android sdk 查询
[android](https://github.com/zguop/ens-android-client)

#### 用 eosjs 查询
// todo

### 客户端协议设计
+ [client-design-en](https://github.com/flyer88/ENS/blob/HEAD/client-design-en.md)
+ [中文版](https://github.com/flyer88/ENS/blob/HEAD/client-design-zh.md)



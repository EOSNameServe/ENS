
## 协议类型
```
ens://[contract-name]
```


## 举例

### 用户输入

`eosio://enserve.bank`

### 客户端处理
请求节点接口，解析数据，返回调用方

**request-url:** 
```
https://node.eosflare.io/v1/chain/get_table_rows
```

**request-params:**
```
{
	"scope":"enserve.bank",
	"code":"enserve.bank",
	"table":"enstables",
	"json":"true"
}
```
**request-result:**
```
[
   "rows": [
        {
            "account_name": "6120580929069623040",
            "dapp": "https://eosnameserve.github.io"
        }
    ],
    "more": false
]
```

**return-result:**  
客户端解析数据，返回 ["https://eosnameserve.github.io"](https://eosnameserve.github.io)



## sdk

+ [android](https://github.com/zguop/ens-android-client)

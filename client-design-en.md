
## protocl
```
ens://[contract-name]
```

## Example

### user input

```
ens://enserve.bank
```

### client processing 
request bp, parse data, give the result to the caller

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
{
    "rows": [
        {
            "account_name": "6120580929069623040",
            "dapp": "https://eosnameserve.github.io"
        }
    ],
    "more": false
}
```
**return-result:**   
client will parse the result，return ["https://eosnameserve.github.io"](https://eosnameserve.github.io)


## sdk

+ [android](https://github.com/zguop/ens-android-client)

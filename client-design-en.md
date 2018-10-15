
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
**url:** `https://node.eosflare.io/v1/chain/get_table_rows`

**params:**
```
{
	"scope":"enserve.bank",
	"code":"enserve.bank",
	"table":"enstables",
	"json":"true"
}
```

**result:**
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

client will parse the result，return ["https://eosnameserve.github.io"](https://eosnameserve.github.io)


# ENS
EOSAccountNameService

# contract
enserve.bank


## usage

### bind 

You can use push an action to `enserve.bank` with action `binddapp`.
Besides, if you want to update it, you can also push this action.

+ use cleos 
```
cleos push action enserve.bank binddapp '["https://eosnameserve.github.io","enserve.bank"]'  -p enserve.bank@active

```

+ use eosjs
// todo




### query

+ use cleos 

```
cleos get table enserve.bank [YOUR_CONTRACT_NAME] enstables
```

example: query `enserve.bank` info.
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

+ use eosjs
// todo


[client-design]()


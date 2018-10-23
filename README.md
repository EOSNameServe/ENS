## ENS
EOSAccountNameService

This is rudiment of DSN over EOSIO.You can bind it over contract, query the url or ip address by rpc or anything can connect to EOSIO.
For exampl, you can [bind](http://eosnameserve.github.io) `enserve.bank` (an EOS MainNet account) with http://eosnameserve.github.io, after that, you can put your eos name to visit your web site by [a chrome plugin](https://github.com/fengqiyue/ensProtocolParser).

## contract
[enserve.bank](https://bloks.io/account/enserve.bank)


## usage

### bind 

You can use push an action to `enserve.bank` with action `binddapp`.
Besides, if you want to update it, you can also push this action.
In fact, you also can bind ip address.

+ use web page
  you need an eos account and scatter plugin.
  [ensnameserve](https://eosnameserve.github.io/#/)

+ use cleos 
```
cleos push action enserve.bank binddapp '["https://eosnameserve.github.io","enserve.bank"]'  -p enserve.bank@active

```

+ use eosjs
// todo




### query

+ use chrome plugin
you can input your eos account, it will refer to your bind url or ip website.
[chrome_plugin](https://github.com/fengqiyue/ensProtocolParser)

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

+ use android sdk
[android](https://github.com/zguop/ens-android-client)

+ use iOS sdk
// todo  

###client design
+ [client-design-en](https://github.com/flyer88/ENS/blob/HEAD/client-design-en.md)
+ [中文版](https://github.com/flyer88/ENS/blob/HEAD/client-design-zh.md)



# EOSMonitor API

EOSMonitor's API is useful to get information about EOS tokens, balances, accounts, contracts, transactions and actions. There is no any warranty for provided data.

## About the API

This is a pre-alpha version, It is not recommended for use in production environments.

## Limit

In most cases, you can send the request directly.

`curl http://api.eosmonitor.io/v1/blocks/100`

This will limit your number of requests per minute, default: 30r/m.

**Please do not overload the servers or you'll be banned.**

If you need more data or highload of service – You need a pro token(Currently not supported).

Then:

`curl https://api.eosmonitor.io/v1/blocks/100?par=par&token={yourtoken}`

## How to view the limit status?

In the head of the response:

* X-Rate-Limit-Limit: 30
* X-Rate-Limit-Remaining: 29
* X-Rate-Limit-Reset: 1533543496

## API URL

* http(s)://api.eosmonitor.io  (For global CDN)
* http(s)://api.coinmeta.cn (For china CDN)

## Response Code

code | message | description
---- | --- | ---
0 | Success | Success
1000 |  Unauthorized | Token error or expired
1001 | Error | System error
1002 | Request exceeded limit | Request exceeded limit
1007 | Invalid parameters | Invalid parameters
1008 | Not Found | Resource does not exist

## Account

### Get Account Info

`GET` `https://api.eosmonitor.io/v1/accounts/<account_name>`
```json
{
    "code": 0,
    "data": {
        "cpu_limit": {
            "available": 232689,
            "max": 242203,
            "used": 9514
        },
        "cpu_weight": 20001,
        "created": "2018-06-10T13:04:21.500",
        "creator": "gy2danrygene",
        "delegated_bandwidth": {
            "cpu_weight": "2.0000 EOS",
            "from": "eosteaeostea",
            "net_weight": "2.0000 EOS",
            "to": "eosteaeostea"
        },
        "eos_balance": 0.0001,
        "last_code_update": "1970-01-01T00:00:00.000",
        "name": "eosteaeostea",
        "net_limit": {
            "available": 1283143,
            "max": 1283375,
            "used": 232
        },
        "net_weight": 20001,
        "permissions": [
            {
                "parent": "owner",
                "perm_name": "active",
                "required_auth": {
                    "accounts": [],
                    "keys": [
                        {
                            "key": "EOS5B7V5TxdZPNiBeDUJSdoovg4Unp3CCbUy4KDiuWJXEWcctXLZN",
                            "weight": 1
                        }
                    ],
                    "threshold": 1,
                    "waits": []
                }
            },
            {
                "parent": "",
                "perm_name": "owner",
                "required_auth": {
                    "accounts": [],
                    "keys": [
                        {
                            "key": "EOS5B7V5TxdZPNiBeDUJSdoovg4Unp3CCbUy4KDiuWJXEWcctXLZN",
                            "weight": 1
                        }
                    ],
                    "threshold": 1,
                    "waits": []
                }
            }
        ],
        "privileged": false,
        "ram_quota": 10449,
        "ram_usage": 4137,
        "total_resources": {
            "cpu_weight": "2.0001 EOS",
            "net_weight": "2.0001 EOS",
            "owner": "eosteaeostea",
            "ram_bytes": 10449
        }
    },
    "error": null,
    "message": "Success"
}
```

## BLock

### Get Block Info
`GET` `https://api.eosmonitor.io/v1/blocks/<block_num_or_id>`

```json
{
    "code": 0,
    "data": {
        "action_mroot": "999e8d1786a7648a513bc6fdc5be12b8ac4f7b0010fa31f6f8cb85f281eea793",
        "bft_irreversible_blocknum": 0,
        "block_id": "0091dcf6cff16bf34c32c5ab92f7906baf85f4209d826a031d9b65869bcdff8e",
        "block_num": 9559286,
        "block_signing_key": "EOS8QgURqo875qu3a8vgZ58qBeu2cTehe9zAWRfpdCXAQipicu1Fi",
        "dpos_irreversible_blocknum": 9558959,
        "dpos_proposed_irreversible_blocknum": 9559127,
        "irreversible": true,
        "pending_schedule_hash": "3016bff9cefb9e4b2dad629478a71c03178ea6acd041845437154db0ef190716",
        "pending_schedule_lib_num": 9514937,
        "previous_block_id": "0091dcf5ecaa49d0d5aaf513cbd6ec0c75acd02c9d5b6082347b79fd36685c1a",
        "producer": "eoslaomaocom",
        "producer_signature": "SIG_K1_KcC6NBme4GfYdSczuwrWKUo5342wuajN6cSkJAJoBrQ22gsG55bfBNsAtVX3iZoCBQzoTyegx1Dinb2Eko38ZtnFT1giAs",
        "schedule_version": 259,
        "timestamp": 1533442735,
        "transaction_mroot": "6749c22bff187c2b8fda8c79eaa03ea6a1b78b5e8e4bc0e2c08233baef3d1348",
        "trx_count": 1
    },
    "error": null,
    "message": "Success"
}
```

## Transaction

### Get Transaction Info

`GET` `https://api.eosmonitor.io/v1/transactions/<transaction_id>`

```json
{
    "code": 0,
    "data": {
        "actions_count": 1,
        "block_id": "00900b3b0a085e701551d5f1a60c2b4897369d7152393ab928d3a52be7e3f328",
        "block_num": 9440059,
        "delay_sec": 0,
        "expiration": 1533410366,
        "irreversible": true,
        "max_cpu_usage_ms": 0,
        "max_net_usage_words": 0,
        "ref_block_num": 2547,
        "ref_block_prefix": 2661908677,
        "signatures": [
            "SIG_K1_JzL2sNqDSUetbzv5uQp8XwV2UwNY49Gvcd7kzVmX2bVAb4CTfPQJQjpGXp1XezgWQ4t38s7mmfjmYoeihT6RZcdzFqCUrr"
        ],
        "signing_keys": [
            "EOS5eexMGYyzwxqzTjJ8x2itT78eFkU9ecEu34kifbLq7QzvrJ88V"
        ],
        "transaction_extensions": [],
        "transaction_id": "c5504cbbb70ce297cffc1bdd9a856e0497f3b64420bdae79063123b3ec3f5186"
    },
    "error": null,
    "message": "Success"
}
```
### Get Transaction Action

`GET` `https://api.eosmonitor.io/v1/transactions/<transaction_id>/actions`

Parameter

Field | Type | Description
--- | --- | ---
page(optional) | Number | Default value: 1
per_page(optional) | Number | Default value: 10

```json
{
    "code": 0,
    "data": {
        "data": [
            {
                "action_num": 0,
                "authorization": [
                    {
                        "actor": "gm2tkmbyguge",
                        "permission": "active"
                    }
                ],
                "data": {
                    "from": "gm2tkmbyguge",
                    "memo": "",
                    "quantity": "0.0001 EOS",
                    "to": "eoslaomaocom"
                },
                "expiration": 1533410366,
                "handler_account": "eosio.token",
                "name": "transfer",
                "trx_id": "c5504cbbb70ce297cffc1bdd9a856e0497f3b64420bdae79063123b3ec3f5186"
            }
        ],
        "has_next": false,
        "has_prev": false,
        "page": 1,
        "per_page": 10,
        "total": 1
    },
    "error": null,
    "message": "Success"
}
```

## Actions

###  Get Actions

`GET` `https://api.eosmonitor.io/v1/actions`

Parameter

Field | Type | Description
--- | --- | ---
account | String | Which account action. Length(1, 12)
name |  String | Action type.Allowed values: "all", "transfer", "sellram", "buyram", "buyrambytes", "setram", "updateauth", "deleteauth", "linkauth", "unlinkauth", "reqauth", "undelegatebw", "delegatebw", "refund", "voteproducer", "regproxy", "rmvproducer", "regproducer", "claimrewards", "unregprod", "setabi", "setcode", "newaccount", "bidname", "create", "issue", "canceldelay", "onerror", "setpriv", "setalimits", "setglimits", "setprods", "setparams", "setparams"
page(optional) | Number | Default value: 1
per_page(optional) | Number | Default value: 10

```json
{
    "code": 0,
    "data": {
        "data": [
            {
                "action_num": 0,
                "authorization": [
                    {
                        "actor": "eosteaeostea",
                        "permission": "active"
                    }
                ],
                "data": {
                    "from": "eosteaeostea",
                    "memo": "",
                    "quantity": "104.9031 EOS",
                    "to": "eostea111111"
                },
                "expiration": 1533398672,
                "handler_account": "eosio.token",
                "name": "transfer",
                "trx_id": "e5ba7e8cd2e0b1ff2522a751e1a05b47b602044395077350f2916528894e8ec8"
            }
        ],
        "has_next": true,
        "has_prev": false,
        "page": 1,
        "per_page": 1,
        "total": 12
    },
    "error": null,
    "message": "Success"
}
```

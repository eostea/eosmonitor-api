# 查询Abi基本信息

## 请求端点

`/v1/abi/:account_name`

## 请求示例

`https://api.eosmonitor.io/v1/abi/eosio.token`

## 返回结果字段说明

| 字段 | 类型 | 描述 |
| --- | --- | --- |
| account      | String       | 合约账户名 |
| abi_extensions   | Array        | |
| actions   | Array        | |
| error_messages   | Array        | |
| ricardian_clauses   | Array        | |
| structs   | Array        | |
| tables   | Array        | |
| types   | Array        | |
| variants   | Array        | |
| version   | String        | |


## 返回结果示例

```json
{
    "code": 0,
    "data": {
        "abi_extensions": [],
        "account": "eosio.token",
        "actions": [
            {
                "name": "transfer",
                "ricardian_contract": "",
                "type": "transfer"
            },
            {
                "name": "issue",
                "ricardian_contract": "",
                "type": "issue"
            },
            {
                "name": "retire",
                "ricardian_contract": "",
                "type": "retire"
            },
            {
                "name": "create",
                "ricardian_contract": "",
                "type": "create"
            },
            {
                "name": "close",
                "ricardian_contract": "",
                "type": "close"
            },
            {
                "name": "extransfer",
                "ricardian_contract": "",
                "type": "extransfer"
            },
            {
                "name": "exissue",
                "ricardian_contract": "",
                "type": "exissue"
            },
            {
                "name": "exretire",
                "ricardian_contract": "",
                "type": "exretire"
            },
            {
                "name": "excreate",
                "ricardian_contract": "",
                "type": "excreate"
            },
            {
                "name": "exclose",
                "ricardian_contract": "",
                "type": "exclose"
            },
            {
                "name": "exdestroy",
                "ricardian_contract": "",
                "type": "exdestroy"
            },
            {
                "name": "exchange",
                "ricardian_contract": "",
                "type": "exchange"
            },
            {
                "name": "ctxrecharge",
                "ricardian_contract": "",
                "type": "ctxrecharge"
            },
            {
                "name": "ctxextract",
                "ricardian_contract": "",
                "type": "ctxextract"
            },
            {
                "name": "ctxtransfer",
                "ricardian_contract": "",
                "type": "ctxtransfer"
            },
            {
                "name": "exunlock",
                "ricardian_contract": "",
                "type": "exunlock"
            },
            {
                "name": "exlocktrans",
                "ricardian_contract": "",
                "type": "exlocktrans"
            }
        ],
        "error_messages": [],
        "ricardian_clauses": [],
        "structs": [
            {
                "base": "",
                "fields": [
                    {
                        "name": "sym",
                        "type": "symbol"
                    },
                    {
                        "name": "contract",
                        "type": "account_name"
                    }
                ],
                "name": "extended_symbol"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "quantity",
                        "type": "asset"
                    },
                    {
                        "name": "contract",
                        "type": "account_name"
                    }
                ],
                "name": "extended_asset"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "from",
                        "type": "account_name"
                    },
                    {
                        "name": "to",
                        "type": "account_name"
                    },
                    {
                        "name": "quantity",
                        "type": "asset"
                    },
                    {
                        "name": "memo",
                        "type": "string"
                    }
                ],
                "name": "transfer"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "issuer",
                        "type": "account_name"
                    },
                    {
                        "name": "maximum_supply",
                        "type": "asset"
                    }
                ],
                "name": "create"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "to",
                        "type": "account_name"
                    },
                    {
                        "name": "quantity",
                        "type": "asset"
                    },
                    {
                        "name": "memo",
                        "type": "string"
                    }
                ],
                "name": "issue"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "quantity",
                        "type": "asset"
                    },
                    {
                        "name": "memo",
                        "type": "string"
                    }
                ],
                "name": "retire"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "owner",
                        "type": "account_name"
                    },
                    {
                        "name": "symbol",
                        "type": "symbol"
                    }
                ],
                "name": "close"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "from",
                        "type": "account_name"
                    },
                    {
                        "name": "to",
                        "type": "account_name"
                    },
                    {
                        "name": "quantity",
                        "type": "extended_asset"
                    },
                    {
                        "name": "memo",
                        "type": "string"
                    }
                ],
                "name": "extransfer"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "issuer",
                        "type": "account_name"
                    },
                    {
                        "name": "maximum_supply",
                        "type": "asset"
                    },
                    {
                        "name": "connector_weight",
                        "type": "float64"
                    },
                    {
                        "name": "maximum_exchange",
                        "type": "asset"
                    },
                    {
                        "name": "reserve_supply",
                        "type": "asset"
                    },
                    {
                        "name": "reserve_connector_balance",
                        "type": "asset"
                    }
                ],
                "name": "excreate"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "to",
                        "type": "account_name"
                    },
                    {
                        "name": "quantity",
                        "type": "extended_asset"
                    },
                    {
                        "name": "memo",
                        "type": "string"
                    }
                ],
                "name": "exissue"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "from",
                        "type": "account_name"
                    },
                    {
                        "name": "quantity",
                        "type": "extended_asset"
                    },
                    {
                        "name": "memo",
                        "type": "string"
                    }
                ],
                "name": "exretire"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "owner",
                        "type": "account_name"
                    },
                    {
                        "name": "symbol",
                        "type": "extended_symbol"
                    }
                ],
                "name": "exclose"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "symbol",
                        "type": "extended_symbol"
                    }
                ],
                "name": "exdestroy"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "primary",
                        "type": "uint64"
                    },
                    {
                        "name": "balance",
                        "type": "extended_asset"
                    }
                ],
                "name": "account"
            },
            {
                "base": "account",
                "fields": [
                    {
                        "name": "lock_timestamp",
                        "type": "time_point_sec"
                    }
                ],
                "name": "lock_account"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "owner",
                        "type": "account_name"
                    },
                    {
                        "name": "quantity",
                        "type": "extended_asset"
                    },
                    {
                        "name": "tosym",
                        "type": "extended_symbol"
                    },
                    {
                        "name": "memo",
                        "type": "string"
                    }
                ],
                "name": "exchange"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "owner",
                        "type": "account_name"
                    },
                    {
                        "name": "quantity",
                        "type": "extended_asset"
                    },
                    {
                        "name": "memo",
                        "type": "string"
                    }
                ],
                "name": "ctxrecharge"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "owner",
                        "type": "account_name"
                    },
                    {
                        "name": "quantity",
                        "type": "extended_asset"
                    },
                    {
                        "name": "memo",
                        "type": "string"
                    }
                ],
                "name": "ctxextract"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "from",
                        "type": "account_name"
                    },
                    {
                        "name": "to",
                        "type": "account_name"
                    },
                    {
                        "name": "quantity",
                        "type": "extended_asset"
                    },
                    {
                        "name": "memo",
                        "type": "string"
                    }
                ],
                "name": "ctxtransfer"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "supply",
                        "type": "asset"
                    },
                    {
                        "name": "max_supply",
                        "type": "asset"
                    },
                    {
                        "name": "issuer",
                        "type": "account_name"
                    },
                    {
                        "name": "max_exchange",
                        "type": "asset"
                    },
                    {
                        "name": "connector_weight",
                        "type": "float64"
                    },
                    {
                        "name": "connector_balance",
                        "type": "asset"
                    },
                    {
                        "name": "reserve_supply",
                        "type": "asset"
                    },
                    {
                        "name": "reserve_connector_balance",
                        "type": "asset"
                    }
                ],
                "name": "currency_stats"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "owner",
                        "type": "account_name"
                    },
                    {
                        "name": "quantity",
                        "type": "extended_asset"
                    },
                    {
                        "name": "expiration",
                        "type": "time_point_sec"
                    },
                    {
                        "name": "memo",
                        "type": "string"
                    }
                ],
                "name": "exunlock"
            },
            {
                "base": "",
                "fields": [
                    {
                        "name": "from",
                        "type": "account_name"
                    },
                    {
                        "name": "to",
                        "type": "account_name"
                    },
                    {
                        "name": "quantity",
                        "type": "extended_asset"
                    },
                    {
                        "name": "expiration",
                        "type": "time_point_sec"
                    },
                    {
                        "name": "memo",
                        "type": "string"
                    }
                ],
                "name": "exlocktrans"
            }
        ],
        "tables": [
            {
                "index_type": "i64",
                "key_names": [
                    "primary"
                ],
                "key_types": [
                    "uint64"
                ],
                "name": "accounts",
                "type": "account"
            },
            {
                "index_type": "i64",
                "key_names": [
                    "currency"
                ],
                "key_types": [
                    "uint64"
                ],
                "name": "stats",
                "type": "currency_stats"
            },
            {
                "index_type": "i64",
                "key_names": [
                    "primary"
                ],
                "key_types": [
                    "uint64"
                ],
                "name": "ctxaccounts",
                "type": "account"
            },
            {
                "index_type": "i64",
                "key_names": [
                    "primary"
                ],
                "key_types": [
                    "uint64"
                ],
                "name": "lockaccounts",
                "type": "lock_account"
            }
        ],
        "types": [
            {
                "new_type_name": "account_name",
                "type": "name"
            }
        ],
        "variants": [],
        "version": "eosio::abi/1.0"
    },
    "message": "Success"
}
```

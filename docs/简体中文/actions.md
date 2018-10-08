# 获取Action

## 请求端点

`/v1/actions`

## 请求参数

| 字段 | 类型 | 必填 | 描述 |
| --- | --- | --- | --- |
| name      | String |   是   | action类型, transfer, sellram, buyram .... |
| account      | String |   是   | 要查询的账户名 |
| page      | Int |   否   | 页数, 默认1 |
| per_page     | Int  | 否 | 每页返回的数据, 默认10 |

## 请求示例

`https://api.eosmonitor.io/v1/actions?name=transfer&account=eosteaeostea`

## 返回结果字段说明

| 字段 | 类型 | 描述 |
| --- | --- | --- |
| account      | String       | 账户名 |
| contract     | String         | 合约账户 |
| quantity      | String        | 代币余额|
| symbol        | String        | 代币符号|


## 返回结果示例

```json
{
    "code": 0,
    "data": {
        "more": true,
        "rows": [
            {
                "account": "eosio.token",
                "authorization": [
                    {
                        "actor": "eosio.bpay",
                        "permission": "active"
                    },
                    {
                        "actor": "eosteaeostea",
                        "permission": "active"
                    }
                ],
                "block_num": 374238,
                "block_time": "2018-08-30T04:44:07.5Z",
                "context_free": false,
                "cpu_usage": 0,
                "data": {
                    "from": "eosio.bpay",
                    "memo": "producer block pay",
                    "quantity": "3770.6717 FO",
                    "to": "eosteaeostea"
                },
                "expiration": "2018-08-30T04:45:06Z",
                "hex_data": "008037f500ea30556054c65419953155dd5b3f020000000004464f00000000001270726f647563657220626c6f636b20706179",
                "id": 560565,
                "name": "transfer",
                "producer_block_id": "0005b5ded5079365d034ddc53eafb4aa720a9eb764f9fe3d8860ffa7bb60b7a0",
                "trx_id": "b74e08b1812abb581fb4ba1767549d1cacf005c91ca79e1f51751cac921241d6"
            },
            {
            "注释": "这里省略了很多..."
            }
        ],
        "total": 208
    },
    "message": "Success"
}
```
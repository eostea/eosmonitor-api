# 获取账户代币列表

## 请求端点

`/v1/accounts/:account_name/coins`

## 请求参数

| 字段 | 类型 | 必填 | 描述 |
| --- | --- | --- | --- |
| page      | Int |   否   | 页数, 默认1 |
| per_page     | Int  | 否 | 每页返回的数据, 默认10 |

## 请求示例

`https://api.eosmonitor.io/v1/accounts/eosteaeostea/coins`

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
        "more": false,
        "rows": [
            {
                "account": "eosteaeostea",
                "contract": "eosio",
                "quantity": "0.7380 EOS",
                "symbol": "EOS"
            }
        ],
        "total": 1
    },
    "message": "Success"
}
```
# 获取交易Action

## 请求端点

`/v1/transactions/:trx_id/actions`

## 请求参数

| 字段 | 类型 | 必填 | 描述 |
| --- | --- | --- | --- |
| page      | Int |   否   | 页数, 默认1 |
| per_page     | Int  | 否 | 每页返回的数据, 默认10 |

## 请求示例

`https://api.eosmonitor.io/v1/transactions/104bb57728b3ad28e9eed18ad4ac5660c0cb7880e9369d1f429c798319b2d45d/actions`

## 返回结果示例

```json
{
    "code": 0,
    "data": {
        "more": true,
        "rows": [
            {
                "action_num": 0,
                "block_num": 1830871,
                "block_time": "2018-09-08T06:20:45.5Z",
                "delay_sec": 0,
                "expiration": null,
                "id": 4731915,
                "max_cpu_usage_ms": 0,
                "max_net_usage_words": 0,
                "producer_block_id": "001befd71043824d3496e3c9e9fb60eac4b595a27320cb011417bb44bca74f7c",
                "receipt": {
                    "cpu_usage_us": 0,
                    "net_usage_words": 0,
                    "status": ""
                },
                "ref_block_num": 0,
                "ref_block_prefix": 0,
                "signatures": null,
                "signed_id": ""
            },
            {
            "注释": "省略..."
            }
        ],
        "total": 18
    },
    "message": "Success"
}
```
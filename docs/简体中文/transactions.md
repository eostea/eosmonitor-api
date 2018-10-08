# 获取Transaction

## 请求端点

`/v1/transactions/:trx_id`

## 请求示例

`https://api.eosmonitor.io/v1/transactions/104bb57728b3ad28e9eed18ad4ac5660c0cb7880e9369d1f429c798319b2d45d`

## 返回结果示例

```json
{
    "code": 0,
    "data": {
        "action_num": 1,
        "block_num": 1830871,
        "block_time": "2018-09-08T06:20:45.5Z",
        "delay_sec": 0,
        "expiration": "2018-09-08T06:21:44Z",
        "id": "104bb57728b3ad28e9eed18ad4ac5660c0cb7880e9369d1f429c798319b2d45d",
        "irreversible": true,
        "max_cpu_usage_ms": 0,
        "max_net_usage_words": 0,
        "producer_block_id": "001befd71043824d3496e3c9e9fb60eac4b595a27320cb011417bb44bca74f7c",
        "receipt": {
            "cpu_usage_us": 10290,
            "net_usage_words": 13,
            "status": "executed"
        },
        "ref_block_num": 61067,
        "ref_block_prefix": 3525603815,
        "signatures": [
            "SIG_K1_KchwMXRYbUaEdhe1tfnbNMkM9ddvFSAKbzgFgrsKa8HgYbUUTgik82XHFS2FCGAW74yLJYBLhwKPmMwScS6Pg6YkRLUVBa"
        ],
        "signed_id": "790e1f223d4814fb9c9cca6142a5a78bd2ed2b49d2343ab9d4cd9cd2b0fe7d3e"
    },
    "message": "Success"
}
```
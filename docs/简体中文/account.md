# 获取账户信息

## 请求端点

`/v1/accounts/:account_name`

## 请求示例

`https://api.eosmonitor.io/v1/accounts/eosteaeostea`

## 返回结果字段说明

| 字段 | 类型 | 描述 |
| --- | --- | --- |
| account_name      | String       | 账户名 |


## 返回结果示例

```json
{
    "code": 0,
    "data": {
        "account_name": "eosteaeostea",
        "cpu_limit": {
            "available": 28521,
            "max": 48203,
            "used": 19682
        },
        "cpu_weight": 1000,
        "created": "2018-08-29T06:55:35.000",
        "head_block_num": 6155366,
        "head_block_time": "2018-10-03T10:00:16.500",
        "last_code_update": "1970-01-01T00:00:00.000",
        "net_limit": {
            "available": 387963,
            "max": 388068,
            "used": 105
        },
        "net_weight": 1000,
        "permissions": [
            {
                "parent": "owner",
                "perm_name": "active",
                "required_auth": {
                    "keys": [
                        {
                            "key": "FO7VjNNh8ro218caH6wzFuk3vJCKaxeaQphdvDb2PjUE3nmKNiVU",
                            "weight": 1
                        }
                    ],
                    "threshold": 1
                }
            },
            {
                "parent": "",
                "perm_name": "owner",
                "required_auth": {
                    "keys": [
                        {
                            "key": "FO7VjNNh8ro218caH6wzFuk3vJCKaxeaQphdvDb2PjUE3nmKNiVU",
                            "weight": 1
                        }
                    ],
                    "threshold": 1
                }
            }
        ],
        "privileged": false,
        "ram_quota": 5475,
        "ram_usage": 4988,
        "total_resources": {
            "cpu_weight": "0.1000 FO",
            "net_weight": "0.1000 FO",
            "owner": "eosteaeostea",
            "ram_bytes": 4075
        }
    },
    "message": "Success"
}
```
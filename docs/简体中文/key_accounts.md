# 获取Key下的账户

## 请求端点

`/v1/keys/get_accounts`

## 请求参数

| 字段 | 类型 | 必填 | 描述 |
| --- | --- | --- | --- |
| public_key     | String  | 是 | 要查询的key |

## 请求示例

`https://api.eosmonitor.io/v1/keys/get_accounts?public_key=FO7VjNNh8ro218caH6wzFuk3vJCKaxeaQphdvDb2PjUE3nmKNiVU`

## 返回结果示例

```json
{
    "code": 0,
    "data": [
        "eosteaeostea"
    ],
    "message": "Success"
}
```
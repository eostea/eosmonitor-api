# 获取Inline Action

## 请求端点

`/v1/actions/:action_id/inline`

## 请求参数

| 字段 | 类型 | 必填 | 描述 |
| --- | --- | --- | --- |
| page      | Int |   否   | 页数, 默认1 |
| per_page     | Int  | 否 | 每页返回的数据, 默认10 |

## 请求示例

`https://api.eosmonitor.io/v1/actions/725714/inline`


## 返回结果示例

```json
{
    "code": 0,
    "data": {
        "more": false,
        "rows": ["结构和action结构相同"],
        "total": 0
    },
    "message": "Success"
}
```
# 获取账户投票信息

## 请求端点

`/v1/accounts/:account_name/vote`

## 请求示例

`https://api.eosmonitor.io/v1/accounts/londonbpfib5/vote`

## 返回结果字段说明

| 字段 | 类型 | 描述 |
| --- | --- | --- |
| is_proxy      | Bool       | 是否为代理帐号 |
| last_vote_weight     | String         |  |
| owner      | String        | 投票账户|
| producers        | Array[String]        | 投的节点|
| proxied_vote_weight | String | 代理的投票权重 |
| staked | String  |    账户抵押量, 最小单位 |
| voter_num | Int | 投票的节点数量|

## 返回结果示例

```json
{
    "code": 0,
    "data": {
        "is_proxy": false,
        "last_vote_weight": "175880767898244.71875000000000000",
        "owner": "londonbpfib5",
        "producers": [
            "aprilfibosbp",
            "bitzebitze11",
            "universalbi1"
        ],
        "proxied_vote_weight": "0E-6176",
        "proxy": "",
        "staked": "383300000",
        "voter_num": 3
    },
    "message": "Success"
}

```
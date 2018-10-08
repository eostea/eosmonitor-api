# 获取区块信息

## 请求端点

`/v1/blocks/:block_id_or_block_num`

## 请求示例

`https://api.eosmonitor.io/v1/blocks/2`


## 返回结果示例

```json
{
    "code": 0,
    "data": {
        "block_num": 2,
        "header": {
            "action_mroot": "0b100beeb61cd9689c3ec2c06b44b4d01d4a52ebd8fa771610079b9bb7c063da",
            "block_signing_key": "EOS6MRyAjQq8ud7hVNYcfnVPJqcVpscN5So8BhtHuGYqET5GDW5CV",
            "previous": "000000018efcb02cbe6329996bdf007c30077907a3fbec119373644a4da3902e",
            "producer_signature": "SIG_K1_K6dARMz2whSqFDfhgDFfRuyQ4HiqNLqTUvq4ykCmzVxKf2rC3CVnqBnWZ5vNYJnG8YAtpA2jri7RG7rs7Ti2AwECw6PYhJ",
            "transaction_mroot": "0000000000000000000000000000000000000000000000000000000000000000"
        },
        "id": "0000000213cadfe48695554f2c642fb4d16314a3a5f57b538959103fafc0bd46",
        "in_current_chain": true,
        "irreversible": true,
        "producer": "eosio",
        "timestamp": "2018-08-28T00:00:00.5Z",
        "trx_count": 0,
        "validated": true
    },
    "message": "Success"
}
```
# 欢迎使用EOSMonitor API

EOSMonitor API 可以被用来获取EOS网络中的区块, 交易, Action, 账户, 账户余额, Token, 合约等信息。

## API URL

EOSMonitor API 地址:
> EOS主网上的数据

* 使用大陆地区CDN
    * http(s)://eosmonitor-api.tc.ink
* 使用海外CDN
    * http(s)://api.eosmontor.io

***

FoMeta API 地址:
> FIBOS主网上的数据

* 使用大陆地区CDN
    * http(s)://fometa-api.tc.ink
* 使用海外CDN
    * http(s)://api.fometa.io
    
## 使用限制

测试Token: dRrJB0iD2Yk3uq1X1lqEN1FzoOWmPltO

本文档除特殊说明的接口之外, 其他每个接口默认都需要携带`token`参数进行授权。比如:

`curl https://api.eosmonitor.io/v1/blocks/100?par=par&token={yourtoken}`

每个接口均按照分钟限制请求次数, 如果超过约定的每分钟请求次数, 相应的`token`将会被服务器限制请求一分钟。

如果一个`token`长时间处于超过请求次数限制的状态(这个Token基本每分钟都会被限制, 实际上大部分时间都处于不可用状态),那么这个`token`将会被永久限制使用。

## 公共响应头

每个请求都会有4个响应头。

* X-RateLimit-Delay: 47
    * 表示在当前的周期内还剩余的时间, 单位秒
    * 一般是最大60, 最小0, 到0之后又会从60从新计数
* X-RateLimit-Limit: 60
    * 目前一个周期允许的最大请求次数
* X-RateLimit-Request: 10
    * 目前周期内已经请求的次数
* X-RateLimit-Remaining: 50
    * 目前周期内剩余的请求次数
    * 随着 `X-Ratelimit-Delay` 每周期重置
* X-Request-Id: 9uJXQiBrT8ye9NohoCB8KkNyDhqxty5a
    * 当前请求的全局唯一ID, 用作调试

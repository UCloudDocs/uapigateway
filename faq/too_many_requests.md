# Too many requests API 流量超过阀值

* 托管在 API 网关共享实例中的 API 具有 QPS限制。共享实例中的 QPS 按 API 分组维度划分，每个分组下所有 API QPS 上限为 1000，超过限额 API 返回 `400` 错误码。
错误信息为 `Too many request`。API 托管方可以在 API 详情中查看请求量监控数据。
* APP 授权场景中，API 托管方可设置时间跨度内调用配额，超过配额会返回 `400` `Too many request` 错误。
* 流量控制场景中，API 托管方可设置单位时间内流量策略。超过流量策略会返回 `400` `Too many request` 错误。

如默认 QPS 限制无法满足现有业务需求，可升级托管集群为独享模式，可致电官方或联系技术支持。


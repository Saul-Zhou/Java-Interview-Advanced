
第一个是高并发，第二个是如何优化

![高性能网关Zuul](/docs/distributed-system/images/gateway-high-concurrency.png)
**Zuul**网关部署的是什么配置的机器，**部署32核64G，对网关路由转发的请求**，**每秒抗个小几万请求是不成问题的，几台Zuul网关机器**

**每秒是1万请求，8核16G的机器部署Zuul网关，5台机器就够了**

### 生产级的网关，应该具备我刚才说的几个特点和功能：

#### (1)动态路由：新开发某个服务，动态把请求路径和服务的映射关系热加载到网关里去；服务增减机器，网关自动热感知
#### (2)灰度发布：基于现成的开源插件来做
#### (3)授权认证
#### (4)限流熔断
#### (5)性能监控：每个API接口的耗时、成功率、QPS
#### (6)系统日志
#### (7)数据缓存






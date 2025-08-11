## 项目详情
### 技术架构

下面这张系统架构图可以帮助大家快速了解 PmHub 项目的系统架构，从前端到网关、从服务应用到基础服务组件、从存储技术到运维部署，可以说是一目了然。

![pmhub-系统架构图](https://cdn.tobebetterjavaer.com/stutymore/01.什么是PmHub-20240708113736.png)

下面这张架构选型图可以帮助大家快速了解 PmHub 项目的技术选型，以及在[官方手册](https://laigeoffer.cn/pmhub/tech-architecture/)中会更详细的说明我们为什么选择该技术，毕竟授人以鱼不如授人以渔嘛。

![pmhub-架构选型](https://cdn.tobebetterjavaer.com/stutymore/PmHub%E6%9E%B6%E6%9E%84%E9%80%89%E5%9E%8B.png)

下面这张技术架构图可以帮助大家快速了解 PmHub 项目的技术架构，以及各个模块之间的交互关系。

![pmhub-技术架构图](https://cdn.tobebetterjavaer.com/stutymore/01.什么是PmHub-20240702103552.png)

优质的项目，离不开一张清晰的鸟瞰图（😄）。

### 项目演示
- 项目仓库（GitHub）：https://github.com/laigeoffer/pmhub
- 项目仓库（码云）：https://gitee.com/laigeoffer/pmhub （国内访问速度更快）
- 项目演示地址：https://pmhub.laigeoffer.cn（微信搜索「苍何」，关注我们的公众号，回复 `pmhub` 获取账号和密码，帮我们增加一个粉丝，哈哈哈，开源不易，请满足一下我的虚荣心（😁）。）

![首页展示](https://cdn.tobebetterjavaer.com/stutymore/20240407163006.png)
![项目概览页](https://cdn.tobebetterjavaer.com/stutymore/202404071500496.png)
![任务编辑页](https://cdn.tobebetterjavaer.com/stutymore/20240407163256.png)
![PmHub表单设计](https://cdn.tobebetterjavaer.com/stutymore/1719456780250-d60beb66-7cd3-4dc5-95c1-893d364ab56a.png)
![PmHub流程设计页面](https://cdn.tobebetterjavaer.com/stutymore/1719458145592-0d855810-b4ca-44c8-a8cc-04b1ac4baa2d.png)

### 代码展示
![pmhub代码展示](https://cdn.tobebetterjavaer.com/stutymore/20240529152747.png)

### 代码结构

```
com.laigeoffer.pmhub     
├── pmhub-ui              // 前端框架 [1024]
├── pmhub-gateway         // 网关模块 [6880]
├── pmhub-auth            // 认证中心 [6800]
├── pmhub-api             // 接口模块
│       └── pmhub-api-system                          // 系统接口
│       └── pmhub-api-workflow                        // 流程接口
├── pmhub-base          // 通用模块
│       └── pmhub-base-core                           // 核心模块组件
│       └── pmhub-base-datasource                     // 多数据源组件
│       └── pmhub-base-seata                          // 分布式事务组件
│       └── pmhub-base-security                       // 安全模块组件
│       └── pmhub-base-swagger                        // 系统接口组件
│       └── pmhub-base-notice                         // 消息组件组件
├── pmhub-modules         // 业务模块
│       └── pmhub-system                              // 系统模块 [6801]
│       └── pmhub-gen                                 // 代码生成 [6802]
│       └── pmhub-job                                 // 定时任务 [6803]
│       └── pmhub-project                             // 项目服务 [6806]
│       └── pmhub-workflow                            // 流程服务 [6808]
├── pmhub-monitor             						  // 监控中心 [6888]                 
├──pom.xml                                            // 公共依赖
```

## 项目部署
> 单体版本请参考：[单体版本部署手册](https://github.com/laigeoffer/pmhub/blob/master/docs/%E6%9C%8D%E5%8A%A1%E5%99%A8%E5%90%AF%E5%8A%A8%E6%95%99%E7%A8%8B.md)
### 环境准备
|    | 技术                  | 名称        | 版本         | 官网                                                                                                 |
|----|---------------------|-----------|------------|----------------------------------------------------------------------------------------------------|
| 1  | Spring Boot         | 基础框架      | 2.7.18     | [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot)                   |
| 2  | SpringCloud         | 微服务框架     | 2021.0.8   | [https://spring.io/projects/spring-cloud](https://spring.io/projects/spring-cloud)                 |
| 3  | SpringCloud Alibaba | 阿里微服务框架   | 2021.0.5.0 | [https://github.com/alibaba/spring-cloud-alibaba](https://github.com/alibaba/spring-cloud-alibaba) |
| 4  | SpringCloud Gateway | 服务网关      | 3.1.8      | [https://spring.io/projects/spring-cloud-gateway](https://spring.io/projects/spring-cloud-gateway) |
| 5  | MyBatis-Plus        | 持久层框架     | 3.5.1      | [https://baomidou.com](https://baomidou.com)                                                       |
| 6  | Redis               | 分布式缓存数据库  | Latest     | [https://redis.io](https://redis.io)                                                               |
| 7  | RocketMQ            | 消息队列      | 2.2.3      | [https://rocketmq.apache.org](https://rocketmq.apache.org)                                         |
| 8  | HuTool              | 小而全的工具集项目 | 5.8.11     | [https://hutool.cn](https://hutool.cn)                                                             |
| 9  | Maven               | 项目构建管理    | 3.9.1      | [http://maven.apache.org](http://maven.apache.org)                                                 |
| 10 | Sentinel            | 流控防护框架    | 1.8.6      | [https://github.com/alibaba/Sentinel](https://github.com/alibaba/Sentinel)                         |
| 11 | Java                | 开发版本      | 1.8        | [https://www.oracle.com/java/technologies](https://www.oracle.com/java/technologies)               |



[MIT License (MIT)](https://opensource.org/licenses/MIT)<hr/>
The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

Copyright (c) 2023-2024 PmHub（苍何、沉默王二）



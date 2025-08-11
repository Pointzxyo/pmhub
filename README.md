<p align="center"><img src= "https://cdn.tobebetterjavaer.com/stutymore/pmhub_%E7%AE%80%E4%BB%8B%E7%89%88.png" alt="MaxKB" width="300" /></p>
<h3 align="center">PmHub，一个基于 SpringCloud & LLM 的智能项目管理系统</h3>
<p align="center">
  <a href="https://opensource.org/license/MIT"><img src="https://img.shields.io/github/license/laigeoffer/pmhub?color=rgb(25%2C%20121%2C%20255)" alt="The MIT License"></a>
  <a href=""><img src="https://img.shields.io/github/forks/laigeoffer/pmhub?color=green" alt="Forks"></a>
  <a href="https://laigeoffer.cn/"><img src="https://img.shields.io/badge/PmHub-%E5%AE%98%E7%BD%91-green" alt="Official"></a>
  <a href="https://github.com/laigeoffer/pmhub"><img src="https://img.shields.io/github/stars/laigeoffer/pmhub?style=flat-square&color=rgb(25%2C%20121%2C%20255)" alt="Stars"></a>    
  <a href="https://pmhub.laigeoffer.cn/"><img src="https://img.shields.io/badge/PmHub-%E4%BD%93%E9%AA%8C%E5%9C%B0%E5%9D%80-blue" alt="Experience"></a>  
</p>

<hr/>
PmHub 是一套基于 SpringCloud & LLM 的微服务智能项目管理系统，这个项目旨在帮助小伙伴们快速掌握微服务/分布式项目的架构设计和开发流程，如果想在校招或者社招中拿到一个满意的 offer，PmHub 将是一个非常 nice 的选择。

## 项目亮点

- **热门技术**：采用时下企业最热门的技术框架，如 SpringCloud-Gateway、Nacos、Sentinel 等，主打一个硬核，与真实的企业项目接轨。
- **单体与微服务**：提供单体和微服务两个版本，完美照顾零基础和需要进阶的同学，带大家体验从单体到微服务架构的改造全过程，并深入理解两种架构的优缺点。
- **硬核面试题**：我们将结合付费球友的实际面试体验，为大家提供可以真正吊打面试官的真是面试场景和题目，并提供 1v1 的简历修改服务，主打一个投了就有、面了就拿 offer 的快乐体感。
- **代码质量**：由蚂蚁金服工作过的技术专家苍何亲自下场，严格遵循代码规范和最佳实践，帮大家养成优雅的代码编写习惯。
- **持续集成**：提供持续集成和持续部署的完整配置，带你从 0-1 用 Docker 上线 生产环境级别的真实项目。
- **产品设计**：[提供完整的产品设计文档](https://lanhuapp.com/link/#/invite?sid=qxZji4oa)，包括产品需求、产品架构、产品原型等，这是别的项目不曾给你的，但工作后又不可或缺的能力。
- **企业工作流**：提供企业级的工作流系统，代码完全开源，你可以在此基础上进行二开，为公司节省巨额的研发成本，从而升职加薪。


## 一、项目简介

PmHub 包括认证、流程、项目管理、用户、网关等服务。包含了 Redis 缓存、RocketMQ 消息队列、Docker 容器化、Jenkins 自动化部署、Spring Security 安全框架、Nacos 服务注册和发现、Sentinel 熔断限流、Seata 分布式事务、Spring Boot Actuator 服务监控、SkyWalking 链路追踪、OpenFeign 服务调用，Vue3 前端框架等互联网开发中需要用到的主流技术栈，可以帮助同学们快速掌握微服务/分布式项目的核心知识点。

并且同时 PmHub 也是一套企业工作流的开发框架，您可以根据自身需求，快速定制出适合自己公司的企业工作流系统。



>如果对开源项目感兴趣，可以关注来个 offer 的另外一个实战项目：技术派，一个前后端分离的社区项目。[GitHub](https://github.com/itwanger/paicoding) 上已经星标 1.5k+，不少同学就是靠这个项目在往年的校招中拿到了不错的 offer。


为了方便大家循序渐进式的学习，我们已经推出两个版本：

- 单体架构版本：适合初学者，直接运行 pmhub-boot 模块下的 pmhub-admin 中的 PmhubApplication 类即可。
- 微服务架构版本：适合有一定基础，想进阶学习微服务/分布式的同学，可以分别启动网关、认证、流程、项目管理、代码生成等多个服务。

可以根据自己的实际情况选择合适的版本进行学习，我们将会倾其所有，在第一时间帮助大家解决所有学习过程遇到的问题，让你的学习曲线变得非常丝滑😁。

* 在线体验地址：https://pmhub.laigeoffer.cn/

![pmhub-业务架构图](https://cdn.tobebetterjavaer.com/stutymore/laigeoffer-pmhub-%E4%B8%9A%E5%8A%A1%E5%A4%A7%E5%9B%BE.png)

此为 PmHub 微服务版本说明文档！单体版本说明文档请移步：[单体版本说明](https://github.com/laigeoffer/pmhub/blob/master/pmhub-boot/README.md)


## 二、项目详情
### 2.1、技术架构

下面这张系统架构图可以帮助大家快速了解 PmHub 项目的系统架构，从前端到网关、从服务应用到基础服务组件、从存储技术到运维部署，可以说是一目了然。

![pmhub-系统架构图](https://cdn.tobebetterjavaer.com/stutymore/01.什么是PmHub-20240708113736.png)

下面这张架构选型图可以帮助大家快速了解 PmHub 项目的技术选型，以及在[官方手册](https://laigeoffer.cn/pmhub/tech-architecture/)中会更详细的说明我们为什么选择该技术，毕竟授人以鱼不如授人以渔嘛。

![pmhub-架构选型](https://cdn.tobebetterjavaer.com/stutymore/PmHub%E6%9E%B6%E6%9E%84%E9%80%89%E5%9E%8B.png)

下面这张技术架构图可以帮助大家快速了解 PmHub 项目的技术架构，以及各个模块之间的交互关系。

![pmhub-技术架构图](https://cdn.tobebetterjavaer.com/stutymore/01.什么是PmHub-20240702103552.png)

优质的项目，离不开一张清晰的鸟瞰图（😄）。

### 2.2、项目演示

![首页展示](https://cdn.tobebetterjavaer.com/stutymore/20240407163006.png)
![项目概览页](https://cdn.tobebetterjavaer.com/stutymore/202404071500496.png)
![任务编辑页](https://cdn.tobebetterjavaer.com/stutymore/20240407163256.png)
![PmHub表单设计](https://cdn.tobebetterjavaer.com/stutymore/1719456780250-d60beb66-7cd3-4dc5-95c1-893d364ab56a.png)
![PmHub流程设计页面](https://cdn.tobebetterjavaer.com/stutymore/1719458145592-0d855810-b4ca-44c8-a8cc-04b1ac4baa2d.png)



### 2.3、代码结构

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



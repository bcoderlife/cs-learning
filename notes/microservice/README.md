# 微服务介绍

微服务架构是一种应用架构类型，其中应用会开发为一系列服务。它提供了独立开发、部署和维护微服务架构图和服务的框架。

在微服务架构中，每个微服务都是独立的服务，旨在容纳一种应用特性并处理离散的任务。每个微服务都通过简单的接口与其他服务通信，以解决业务问题。

## 简述

### 微服务定义

* 基于业务构建的一组单个体量小的服务
* 进程独立，可独立部署，且非集中式管理

```
技术栈，网络，存储等因业务各异
```

* 轻量级，无限制通信

```
所谓轻量级通信机制，通常是指与语言无关、与平台无关的这类协议。通过轻量级通信机制，使服务与服务之间的协作变得简单、标准化
```

### 微服务优缺点

#### 优点：

* 强化服务边界

```
模块边界由原来的类、类库组件变化为一个个的独立服务
```

* 可独立部署

```
每个微服务根据需求独立开发测试上线部署
```

* 技术选型多样

```
容错不同团队的不同语言、框架技术
```

#### 缺点：

* 架构复杂度高

> *成百上千个微服务之间的交互、管理*

* 一致性

> *微服务没有集中式的管理，重要的数据需要维护一致性*

* 后期运维难度高

> *微服务之间的调用链路复杂，需要有专业的监控来发现和排查问题*

* 测试工作复杂

> *不同于传统的大模块测试，分布在大量微服务上的功能点，不能简单按单个服务测试，而是串联起多个微服务，甚至是全链路测试*


## 微服务业务架构

由传统的：

^  
| &ensp; 产 &ensp;&ensp; 研 &ensp;&ensp; 测 &ensp;&ensp; 数 &ensp;&ensp; 运  
| &ensp; 品 &ensp;&ensp; 发 &ensp;&ensp; 试 &ensp;&ensp; 据 &ensp;&ensp; 维  
| &ensp; 团 &ensp;&ensp; 团 &ensp;&ensp; 团 &ensp;&ensp; 团 &ensp;&ensp; 团  
| &ensp; 队 &ensp;&ensp; 队 &ensp;&ensp; 队 &ensp;&ensp; 队 &ensp;&ensp; 队  
|_______________>  
 产 &ensp;&ensp; 品 &ensp;&ensp; A ...  
 产 &ensp;&ensp; 品 &ensp;&ensp; B ...  
 产 &ensp;&ensp; 品 &ensp;&ensp; C ...  

到微服务的：

^  
| &ensp; 产品团队 &ensp;&ensp; 产品团队 &ensp;&ensp; 产品团队 &ensp;&ensp; 平台  
| &ensp; 研发团队 &ensp;&ensp; 研发团队 &ensp;&ensp; 研发团队 &ensp;&ensp; 支撑  
| &ensp; 测试团队 &ensp;&ensp; 测试团队 &ensp;&ensp; 测试团队 &ensp;&ensp; 团队  
| &ensp; 数据团队 &ensp;&ensp; 数据团队 &ensp;&ensp; 数据团队 &ensp;&ensp; ...  
| &ensp; 运维团队 &ensp;&ensp; 运维团队 &ensp;&ensp; 运维团队 &ensp;&ensp; ...  
|______________________________________>  
  产品A  &ensp;&ensp;  产品B &ensp;&ensp;  产品C  

## 微服务技术架构

![微服务技术架构](https://github.com/bcoderlife/cs-learning/blob/master/assets/microservice/microservice-tech-arch.png)



## 微服务核心组件

|  组件   | Spring Cloud | 其他 |
|  ----  | ----  | ---- |
| 服务注册  | Eureka/Zookeeper | Nacos/Consul |
| 配置中心  | Zookeeper/Consul | Apollo/Nacos/ETCD |
| 网关路由  | Zuul/Gateway | Kong/Traefik/APISIX |
| 负载均衡  | Ribbon | Loadbalancer |
| 熔断限流  | Hystrix | Resilience4J/Sentinel |
| 服务监控  | SpringBootAdmin | Prometheus/ES |
| 链路监控  | Zipkin/Sleuth | SkyWalking/Opentracing |
| 消息队列  | Kafka | RocketMQ |
| 服务调用  | Feign/OpenFeign | RestTemplate |


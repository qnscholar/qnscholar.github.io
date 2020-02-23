---
layout: post
title: "SpringCloud"
date: 2019-06-01
description: "SpringCloud原理"
tag: 复习
---
### 1.ribbon的负载均衡
Load Balance负载均衡是用于解决一台机器(一个进程)无法解决所有请求而产生的一种算法。
#### 1.负载均衡的好处
当集群里的1台或者多台服务器down的时候，剩余的没有down的服务器可以保证服务的继续使用。  
使用了更多的机器保证了机器的良性使用，不会由于某一高峰时刻导致系统cpu急剧上升。
#### 2.常见的负载均衡策略
随机 (Random)、轮询 (RoundRobin)、一致性哈希 (ConsistentHash)、哈希 (Hash)、加权（Weighted）。
#### 3.ribbon与eureka的交互过程
`LoadBalancerClient（RibbonLoadBalancerClient是实现类）`在初始化的时候（execute方法），会通过`ILoadBalance（BaseLoadBalancer是实现类）`向Eureka注册中心获取服务注册列表，
并且每10s一次向EurekaClient发送“ping”，来判断服务的可用性，如果服务的可用性发生了改变或者服务数量和之前的不一致，则从注册中心更新或者重新拉取。LoadBalancerClient有了
这些服务注册列表，就可以根据具体的IRule来进行负载均衡。
#### 4.ribbon的负载均衡策略
```
public interface IRule{
    public Server choose(Object key);
    public void setLoadBalancer(ILoadBalancer lb);
    public ILoadBalancer getLoadBalancer();   
}
```
IRule的实现借口有：RandomRule表示随机策略、RoundRobinRule表示轮询策略、WeightedResponseTimeRule表示加权策略、BestAvailableRule表示请求数最少策略等等。  
默认情况下会采用轮询策略
#### 5.参考文献
[Ribbon的负载均衡策略及原理](https://blog.csdn.net/wudiyong22/article/details/80829808)
### 2.feign原理
封装了http调用过程，更适合面向接口化的开发工作。它以Java接口注解的方式调用Http请求，而不用像Java中通过封装HTTP请求报文的方式直接调用。Feign通过处理注解，将请求模板化，
当实际调用的时候，传入参数，根据参数再应用到请求上，进而转化成真正的请求，这种请求相对而言比较直观。
#### 1.feign的调用过程
![feign调用过程](/images/article/spring/feign-process.jpg)
① 在使用feign 时，会定义对应的接口类，在接口类上使用Http相关的注解，标识HTTP请求参数信息。在Feign 底层，通过基于面向接口的动态代理方式生成实现类，将请求调用委托到动态代理实现类。  
② 根据传入的Bean对象和注解信息，从中提取出相应的值，来构造HttpRequest 对象。  
③ 使用Encoder 将Bean转换成 Http报文正文（消息解析和转码逻辑）,Feign 最终会将请求转换成Http 消息发送出去，传入的请求对象最终会解析成消息体。  
④ 基于重试器发送HTTP请求，Feign 内置了一个重试器，当HTTP请求出现IO异常时，Feign会有一个最大尝试次数发送请求（默认5）。  
⑤ 发送Http请求，Feign 默认底层通过JDK 的 java.net.HttpURLConnection 实现了feign.Client接口类,在每次发送请求的时候，都会创建新的HttpURLConnection 链接，这也就是为什么
默认情况下Feign的性能很差的原因。可以通过拓展该接口，使用Apache HttpClient 或者OkHttp3等基于连接池的高性能Http客户端。
#### 2.参考文献
[feign官方](https://github.com/OpenFeign/feign) [Spring Cloud Feign设计原理](https://www.jianshu.com/p/8c7b92b4396c) [springCloud feign的分析](https://blog.51cto.com/13981400/2286765)
### 3.eureka
#### 1.eureka的一些概念
Register：服务注册。当Eureka客户端向Eureka Server注册时，它提供自身的元数据，比如IP地址、端口，运行状况指示符URL，主页等。  
Renew：服务续约。Eureka客户会每隔30秒发送一次心跳来续约。正常情况下，如果Eureka Server在90秒没有收到Eureka客户的续约，它会将实例从其注册表中删除。  
Fetch Registries：获取注册列表信息。Eureka客户端从服务器获取注册表信息，并将其缓存在本地(（每30秒钟）更新一次)。客户端会使用该信息查找其他服务，从而进行远程调用。  
#### 2.原理
服务注册其实很简单，在EurekaClient启动的时候，将自身的服务的信息发送到EurekaServer。在DiscoveryClient类有一个服务注册的方法register()，该方法是通过Http请求向EurekaServer注册。



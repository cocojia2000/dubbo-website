---
type: docs
title: "使用说明"
linkTitle: "使用说明"
weight: 2
---
## 特性说明
当前 dubbo 支持的 thrift 协议是对 thrift 原生协议的扩展，在原生协议的基础上添加了一些额外的头信息，比如 service name，magic number 等。`2.3.0` 以上版本支持。

[Thrift](http://thrift.apache.org) 是 Facebook 捐给 Apache 的一个 RPC 框架。

使用 dubbo thrift 协议同样需要使用 thrift 的 idl compiler 编译生成相应的 java 代码，后续版本中会在这方面做一些增强。

## 使用场景

适用于 SOA 标准 RPC 框架。

## 使用方式

#### 依赖
```xml
<dependency>
    <groupId>org.apache.thrift</groupId>
    <artifactId>libthrift</artifactId>
    <version>0.8.0</version>
</dependency>
```

所有服务共用一个端口：

与原生Thrift不兼容
```xml
<dubbo:protocol name="thrift" port="3030" />
```

 [dubbo 项目中的示例代码](https://github.com/apache/dubbo/tree/master/dubbo-rpc/dubbo-rpc-thrift/src/test/java/org/apache/dubbo/rpc/protocol/thrift)

#### 提示：
* Thrift 不支持 null 值，即：不能在协议中传递 null 值

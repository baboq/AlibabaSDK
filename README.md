# 阿里巴巴SDK For PHP

## 概述

本PHP SDK适用于调用阿里巴巴旗下各开放平台的API。目前已经支持：

* [淘宝开放平台API](http://open.taobao.com/api/api_list.htm?spm=a219a.7386653.1.30.MYVxfa)
* [淘宝开放平台OAuth登录](http://open.taobao.com/doc/detail.htm?id=102635&spm=a219a.7386781.1998342838.19.ryTNmv)
* [阿里云API](http://develop.aliyun.com/api/?spm=5176.100054.201.108.UyKD0b)。目前支持ECS和RDS，理论可进行进一步扩展。


## 特性

* 轻量级胶水层、紧凑型设计，新手进阶均相宜
* 完整的单元测试代码
* 符合PSR-4载入方式，预留Composer接入模式
* 内置的依赖注入（Service Locator实现）可快速调用相关Client

## 协议

使用Apache License, Version 2.0协议。


```

Copyright 2015 Horse Luke

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

```

## 系统要求

* PHP 5.4或以上
* PHP启用Curl扩展、且安装了OpenSSL（因为要调用HTTPS）

## 使用方法

以下目录有使用方法：

* demo目录：是最原始的使用方法，不依赖任何载入方式

* tests目录下的所有“Example2”开头的目录：根据不同接口和Client进行的测试

建议为不同的api接口、注册不同的Client类实例，方法有：

* 使用工厂模式 + 单例模式。

* 使用依赖注入（Dependency Injection）中的Service Locator + 单例模式。

  - 有关Service Locator介绍，可以看 [Github silexphp/Pimple](https://github.com/silexphp/Pimple ) README.md中“Defining Services“部分。
  
  - 如果自己的框架没有实现，可使用SDK已经实现的简单Service Locator：\AlibabaSDK\Integrate\ServiceLocator。
  
    详细用法见目录/demo/Integrate/ServiceLocatorBasicUsage.php


## 文档

（正在撰写中）

## 参赛说明

本作品为2015"云朵之上，编码未来"[阿里云开源编程马拉松](http://bbs.aliyun.com/read/256663.html?spm=5176.100131.1.6.urYu37)参赛作品之一，根据比赛规则，托管在[Git@OSC](http://www.oschina.net/2015-ali-hackathon#item-rule)上。

该参赛作品应看作半学术半工程化作品。该含义是：

* 半学术：由于SDK的特殊性质，若不进行实际应用集成，则可用性不高，仅能作为API架构规范和相关实现的研究。

* 半工程化：本SDK实际可用，能集成在符合运行环境的任何项目中，并且在编码过程中以工业界的工程形式进行了完整的编码和测试。

基于该SDK的工业化实际应用集成开源参赛作品，正在开发中。


![攒钱买房](http://7xlz3z.com1.z0.glb.clouddn.com/img/git/apavqmok7au6ummhae.png)
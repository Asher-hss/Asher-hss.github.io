---
layout:     post
title:      "Kafka Study Notes"
subtitle:   "对于项目中使用的Kafka的记录"
data:       2024-02-07
author:     Asher
header-img: "img/post-bg-os-metro.jpg"
catalog:    true
tags:       
    - Kafka
    - SpringBoot
---
<br>kafka contains topics, topics contains partitions.

<br>various partitions can be deployed on different servers.

<br>kafka use key_value format to store record.

<br>a consumer can consume multiples partitions, but A partition cannot be consumed simultaneously by multiple consumers within the same consumer group.

<br>Kafka中到处都是“批量和异步”设计，它更关注的是整体的吞吐量，而RocketMQ的设计选择更多的是尽量及时处理请求。

<br>比如发消息，同样是用户调用了send()方法，RockMQ它会直接把这个消息发出去，而Kafka会把这个消息放到本地缓存里面，然后择机异步批量发送。

<br>所以，RocketMQ它的时延更小一些，而Kafka的吞吐量更高。
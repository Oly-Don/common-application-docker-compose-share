## 应用介绍-product introduce
- 1. kafka 中间件,常用于消息处理

## 使用要求
- 1. 不使用默认zookeeper的话,修改实际的zookeeper地址;KAFKA_ZOOKEEPER_CONNECT: zookeeper:2181
- 2. 需要定义kafka主机名称IP;KAFKA_ADVERTISED_HOST_NAME: 192.168.99.100

### 优化内容-optimize index
- 1. 无

### 连接
- 1. 宿主IP+9092 ,  kafka
- 1. 宿主IP+2181 ,  kafka中的zookeeper
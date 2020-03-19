## 应用介绍-product introduce
- 1. redis  默认版本:4.0


## 使用要求
- 1. 集群版,严格按照步骤执行,可创建三主三从的待验证的redis stanalone集群;注意关闭防火墙,不然最后的加入集群会挂起造成集群失败且后续不可再次集群化.
- 2. 单机版,直接使用redissingle-docker-compose.yml

### 优化内容-optimize index
- 1. 单机版修改默认端口;  - 7379:6379

### 连接
- 1. 单机版 redis:  宿主IP+7379 ,  密码:u6hCwUvd0w7uwjloHEPgVhwej65HTw
- 1. 集群版 redis:  宿主IP+7000,7001,7002,7003,7004,7005 ,  密码:u6hCwUvd0w7uwjloHEPgVhwej65HTw
## 应用介绍-product introduce
- 1. zookeeper  默认版本: 3.4.12

### 优化内容-optimize index
- 1. 单节点集群版:目前保留10份日志和快照,每五小时执行一次 ;   修改配置:ZOO_AUTOPURGE_PURGEINTERVAL: 5   ZOO_AUTOPURGE_SNAPRETAINCOUNT: 10

```
官方清理日志和快照的设置无效,修改配置
# 以下仅介绍实现细节,注意不再需要修改
sed -ri '/ZOO_MAX_CLIENT_CNXNS/aecho "autoPurge.purgeInterval=$ZOO_AUTOPURGE_PURGEINTERVAL" >> "$CONFIG"\necho "autoPurge.snapRetainCount=$ZOO_AUTOPURGE_SNAPRETAINCOUNT" >> "$CONFIG"' /docker-entrypoint.sh
```

### 连接
- 1. 单节点: 宿主IP+2181    无验证
- 2. 集群和官方:  宿主IP+2181,2182,2183    无验证


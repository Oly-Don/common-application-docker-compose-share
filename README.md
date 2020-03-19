## 基本使用
```

 启动:  docker-compose -f ***/docker-compose.yml up -d
 停止:  docker-compose -f ***/docker-compose.yml stop
 查看后台的一些输出日志:  docker-compose -f ***/docker-compose.yml logs -f
 修改配置后,重加载文件,重启:  docker-compose -f ***/docker-compose.yml up -d --build && docker-compose -f ***/docker-compose.yml restart


 #完全清理容器和其他网络文件挂载   docker-compose -f ***/docker-compose.yml down (备注: -v 会完全清理本地文件和网络设置,不再保留任何容器产生的数据)

 ( A***/docker-compose.yml 为全路径的编排文件地址,尽可能在docker-compose.yml这一级目录操作.)

```

## 修改内容
-  1. 统一使用随机密码 u6hCwUvd0w7uwjloHEPgVhwej65HTw (可能产生的问题,已设置的密码比实际应用要求的长) ; 统一使用IP 192.168.99.100;
-  2. 删除敏感资料,例如 id passwd 域名  局域网ip 广域网域名  IP  姓名  证书 密钥 项目名称
-  3. 样例-**.conf 经供参考,实际中docker-compose.yml 可能会使用到这些文件,注意修改名称去掉"样例-" 字眼.
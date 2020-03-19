## 应用介绍-product introduce
- oracle-jdk:jdk-8u112

## 使用要求
- 1. jar或者war二选一使用;
- 2. jar 部署的方式:
     挂载了配置文件,必须准备好文件: /opt/dubbo/dubbo.war
     挂载了配置文件,必须准备好文件: /opt/dubbo/dubbo.properties
- 3. jar 部署的方式:
     挂载了配置文件,必须准备好文件: /opt/dubbo/dubbo-admin-0.0.1-SNAPSHOT.jar
     挂载了配置文件,必须准备好文件: /opt/dubbo/application.properties
- 4. application.properties 中定义了登陆使用的用户密码以及连接注册中心zookeeper的地址,注意修改成实际值;
```
     ##设置登陆密码
     spring.root.password=u6hCwUvd0w7uwjloHEPgVhwej65HTw
     spring.guest.password=u6hCwUvd0w7uwjloHEPgVhwej65HTw
     #dubbo.registry.address zookeeper的任意一个节点地址
     dubbo.registry.address=zookeeper://192.168.99.100:2181
```
- 4.

### 优化内容-optimize index
- 1. 默认使用包内的配置文件,可以在启动用户下的工作目录放置properties 来使用自定义配置
```
     默认使用包内的配置文件:  dubbo-admin-0.0.1-SNAPSHOT.jar\BOOT-INF\classes\application.properties
     默认使用包内的配置文件:  dubbo.war\WEB-INF\classes\dubbo.properties
     优先级: 服务启动用户的根目录下 properties (领先) > 包内的properties
```


### 连接
- 1. jar  IP+7001/
- 2. war  IP+8080/dubbo/
- 3. 密码默认设置为: u6hCwUvd0w7uwjloHEPgVhwej65HTw 连接的zookeeper默认为192.168.99.100:2181
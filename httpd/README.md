## 应用介绍-product introduce
- oracle-jdk:jdk-8u112

## 使用要求
- 1. Dockerfile-diyhttpd中定制了默认用户 用户组 ,启动绑定端口为20022
- 2. 挂载了配置文件,用于httpd默认的工作目录,注意修改:
```
      - /opt/snweb/psp/www/:/usr/local/apache2/htdocs/:rw  #/opt/snweb/psp/www/ 改为需要访问的父目录
```

### 优化内容-optimize index
- 1. 安全加固,默认服务端口由 80 改为20022;工作用户和用户组由默认的 daemon 改为 ftp;主要挂载进容器的目录权限.
```
	mkdir -p  /etc/httpd/logs && \
	touch /etc/httpd/logs/error.log && \
	sed -i 's/User daemon/User ftp/g' /usr/local/apache2/conf/httpd.conf && \
	sed -i 's/Group daemon/Group ftp/g' /usr/local/apache2/conf/httpd.conf && \
	sed -i 's/Listen 80/Listen 20020/g' /usr/local/apache2/conf/httpd.conf && \
	sed -i '1a\ServerName 192.168.99.100:20020' /usr/local/apache2/conf/httpd.conf && \
```


### 连接
- 1. jar  IP+7001/
- 2. war  IP+8080/dubbo/
- 3. 密码默认设置为: u6hCwUvd0w7uwjloHEPgVhwej65HTw 连接的zookeeper默认为192.168.99.100:2181
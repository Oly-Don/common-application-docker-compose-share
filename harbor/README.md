## 应用介绍-product introduce
- Harbor 企业版的docker镜像仓库
-
## 使用要求
- 1. 准备文件 harbor-offline-installer-v1.7.5.tgz
```
安装条件：
离线安装包harbor-offline-installer-v1.7.5
安装docker、docker-compose

#正式安装：
tar -zxvf harbor-offline-installer-v1.7.5.tgz -C /opt/harbor

#修改关键配置
vi /opt/harbor/harbor.cfg
    ##真实ip
    hostname = 10.10.101.42

#安装
./install.sh
curl 127.0.0.1:80/harbor



#部分说明:
安装过程出错,如何彻底清除数据库：
cat /opt/harbor/docker-compose.yml |grep --color -A 2 volu (删除挂载文件,小心也会删除镜像数据)

##初始化密码为 admin/u6hCwUvd0w7uwjloHEPgVhwej65HTw

```

### 连接
- 1. 地址  宿主IP:80/harbor
- 2. 默认用户密码 admin u6hCwUvd0w7uwjloHEPgVhwej65HTw
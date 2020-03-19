## 应用介绍-product introduce
- 1. jenkins 持续集成的平台,众多插件支持从开发/测试/部署的各种要求

## 使用要求
- 1. 默认版本2.60.3;根据实际要求修改版本; 当前时间最新可使用: FROM jenkins:latest
- 2. agent 文件夹,需要部署主从角色时,从主机上去使用;(主从暂未上传资料,后续补充)

### 优化内容-optimize index
- 1. 修改默认端口;        - '8018:8080'
- 2. 修改默认context;方便反向代理;   JENKINS_OPTS="--prefix=/jenkins/
- 3. 预装常用工具;  apt-get install -y  git maven ant jdk8
- 4. 时区优化
- 5. maven 配置文件挂载; (目前暂时没启用 settings.xml /usr/share/maven/conf/settings.xml)
- 6. 挂载外部docker,所以内部容器能使用到外部的docker

### 连接
- 1. 宿主IP+8018/jenkins/ ,  用户密码登陆后设置
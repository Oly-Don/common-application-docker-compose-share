## 应用介绍-product introduce
- 1. mongo 文档型数据库; 默认版本:3.4

## 使用要求
- 1. 默认存放数据库文件的目录为:宿主/data/mongocontainer
- 2. 默认不开启验证,如需开启的步骤:

```
# 启动后新建库 / 用户 / 密码 / 给用户赋每个新建库的读写权限
# docker-compose.yml up -d
# use admin
# db.createUser({user:"mongousername",pwd:"mongousernameQwe!23",roles:[{role:"root",db:"admin"}]})
# db.auth("mongousername","mongousernameQwe!23")
# use slalog
# db.createUser({user:"mongousername",pwd:"mongousernameQwe!23",roles:[{role:"dbOwner",db:"slalog"}]})
# db.auth({user:"mongousername",pwd:"mongousernameQwe!23"})
# docker-compose.yml down
# 开启验证并启动
去除#
#    command: "--auth"
# docker-compose.yml up -d
```

### 优化内容-optimize index
- 1. 修改默认端口;      - "17017:27017"
- 2. 默认不挂载web管理端口 28017

### 连接
- 1. 宿主IP+17017 ,  默认无需验证,可参见上面内容自行开启验证.
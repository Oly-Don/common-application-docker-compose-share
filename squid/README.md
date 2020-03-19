## 应用介绍-product introduce
- 1. sonarqube  默认版本:最新


## 使用要求
- 1.  端口号为3128,不可被占用
- 2.  如需要自定义配置,请修改
```
#      - /opt/squid3container/squid.conf:/etc/squid3/squid.conf
改为:
      - (实际的配置地址)/opt/squid3container/squid.conf:/etc/squid3/squid.conf(固定)
```

### 优化内容-optimize index
- 1. 无

### 连接
- 1. squid:  宿主IP+3128 , 默认未设置用户密码.
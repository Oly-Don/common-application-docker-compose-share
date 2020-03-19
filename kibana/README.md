## 应用介绍-product introduce
- 1. kibana elk中的k,目前只用到对数据库数据的统计分析

## 使用要求
- 1. 挂载了配置文件,一定要放置配置文件在/opt/kibana_install/kibana.yml  ;       - /opt/kibana_install/kibana.yml:/usr/share/kibana/config/kibana.yml
- 2. 需要定义使用的数据源,elasticsearch地址;    ELASTICSEARCH_HOSTS: http://127.0.0.1:9002

### 优化内容-optimize index
- 1. 无

### 连接
- 1. 宿主IP+5601 ,  kibana
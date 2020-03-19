## 应用介绍-product introduce
- 1. logstash elk中的l,目前主要用到数据格式转换功能,默认版本logstash 6.4.3

## 使用要求
- 1. logstash.yml中修改elasticsearch的实际地址 ;  http://192.168.99.100:9200
- 2. jvm.options 调整启动的JVM参数: -Xms2g -Xmx2g
- 3. /opt/logstash/pipeline/中为pipline的父目录,必须放pipline格式的文件;(容易出错)

### 优化内容-optimize index
- 1. 默认加大JVM参数; -Xms2g -Xmx2g
- 2. 默认关闭XPACK_MONITORING_ENABLED

### 连接
- 1.